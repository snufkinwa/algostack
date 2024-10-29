## Sailor Scouts’ Daily Meeting Schedule Merge

<p align ="center">
<img src = "https://media1.tenor.com/m/fj0ERixWjnsAAAAC/sailor-moon-eat.gif">
</p>

Let's put this into practice. The sailor scouts want to see each other each day, the meeting time is stored in a tuple `(start_time, end_time)` represented by an integer of 30 minute blocks pass 9:00 am, when school starts.

```python
(2,3) # Meeting from 10:00 - 10:30 am
(6, 9) # Meeting from 12:00 - 1:30 pm
```

The goal is to merge overlapping meeting times to give the Sailor Scouts a clear view of when everyone is available for team meetings without any scheduling conflicts.

```python
# Given these meeting times
[(0, 1), (3, 5), (4, 8), (10, 12), (9, 10)]
# Output
[(0, 1), (3, 8), (9, 12)]
```

When answering questions, it’s important to include **pseudocode** to clearly outline our thought process without jumping straight into the code. Most assessments prioritize understanding our approach, so even if we don’t have time to pass every test case, the recruiter can still see our problem-solving strategy.

```python
'''
1. Sort the list of meetings by start time.

2. Start merged_meetings with the first meeting from the sorted list.

3. For each remaining meeting:
    a. Check if it overlaps with the last meeting in merged_meetings:
        - If it does, update the end time of the last meeting to the later end time.
        - If it doesn’t, add it to merged_meetings as a new entry.

4. Return merged_meetings.
'''
```

This approach builds a clear solution structure. Remember, a strong skeleton can be more valuable than perfect code syntax.

<p align ="center">
<img src = "https://media.tenor.com/XP35krvMmWkAAAAi/sailor-moon.gif">
</p>
