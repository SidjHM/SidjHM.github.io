---
layout: post
title: Lab 1: Digimon
subtitle: My Process
cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/thumb.png
share-img: /assets/img/path.jpg
tags: [books, test]
author: Siddhant Jain
---

In this blog post, I’ll walk you through how I analyzed Digimon data using Python to answer three key questions: calculating the average HP of all Digimon, counting Digimon with specific attributes, and building a Digimon team with memory and attack constraints. Along the way, I'll share what worked well, where I ran into issues, and what I learned.

**Finding the Average HP of All Digimon**
The first task was to calculate the average HP of all Digimon. My initial thought was to simply loop through the data, sum up the HP values, and divide by the total number of Digimon.

**Loading the Data**
I used Python's `csv.DictReader()` function to load the Digimon data into a list of dictionaries. Each row in the CSV file corresponded to a Digimon with attributes like HP, Atk, and Memory. This part went smoothly—`csv.DictReader()` is very intuitive for handling CSV files.

**Summing HP Values**
The next step was to iterate through the dataset, sum the HP values, and keep count of how many Digimon I had processed to calculate the average.

```python
def average_hp(digimon_data):
    total_hp = 0
    count = 0
    for digimon in digimon_data:
        total_hp += int(digimon['HP'])
        count += 1
    return total_hp / count
```

**Result**
Once the function ran correctly, it returned an average HP of **1210.88**. Overall, this part went well, but I did encounter an issue where I initially forgot to cast the HP values from strings to integers. After fixing that, it was smooth sailing.

**Counting Digimon by Specific Attributes**
Next, I needed to count how many Digimon had certain attributes, like being of the "Vaccine" type. I wanted a flexible function that could count by any attribute, such as Type or Level.

**Generalizing the Function**
I wrote a function that takes two arguments: the attribute to search by (e.g., "Type") and the specific value to count (e.g., "Vaccine"). This function loops through the data, checks for matches, and increments a counter.

```python
def count_digimon(attribute, value):
    count = 0
    for digimon in digimon_data:
        if digimon[attribute] == value:
            count += 1
    return count
```

**Result**
For example, using this function to count "Vaccine"-type Digimon returned **70**. This was fairly straightforward, and the general structure made it easy to adapt the function for other attributes. No major challenges here.

**Building a Digimon Team with Memory and Attack Constraints**
This was the trickiest part of the project—building a team of up to three Digimon that stays under a memory limit of 15 and has a combined attack (Atk) of at least 300. 

**Iterating Through Combinations**
To approach this, I wrote a function that iterates through combinations of three Digimon and sums their memory and attack values. If the total memory was under 15 and the attack was at least 300, the team was saved to a list of possible teams.

```python
def find_team(digimon_data, memory_limit=15, min_total_atk=300):
    possible_teams = []
    for digimon1 in digimon_data:
        for digimon2 in digimon_data:
            if digimon1 == digimon2: continue
            for digimon3 in digimon_data:
                if digimon3 in [digimon1, digimon2]: continue
                team_memory = int(digimon1['Memory']) + int(digimon2['Memory']) + int(digimon3['Memory'])
                team_atk = int(digimon1['Atk']) + int(digimon2['Atk']) + int(digimon3['Atk'])
                if team_memory <= memory_limit and team_atk >= min_total_atk:
                    possible_teams.append((digimon1['Digimon'], digimon2['Digimon'], digimon3['Digimon'], team_atk, team_memory))
    return possible_teams
```

**Challenges**
One issue I encountered was ensuring that no Digimon was repeated in a team, which required some extra checks in the nested loops. Initially, I didn't account for duplicates, which skewed the results. I fixed this by adding a condition to make sure each Digimon in a team was unique.

**Result**
Eventually, I found several valid teams, like **Kuramon, Pabumon, and Ogremon** with a total attack of **310** and memory usage of **12**. However, the function isn't very efficient, as it checks every possible combination. For larger datasets, I’d need to optimize it by using better algorithms.

**Answers HP**: 1210.8835341365461
**Possible team**: Team: Kuramon, Pabumon, Ogremon | Total Atk: 310, Total Memory: 12
