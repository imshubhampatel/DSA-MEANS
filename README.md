# DSA-MEANS
# Meeting Room Scheduler

## Problem Statement

Imagine you have a series of meetings, each with a start and end time. The goal is to determine the minimum number of rooms required so that no two overlapping meetings are scheduled in the same room.

## Solution Overview

To solve this problem, we treat each meeting as an interval defined by its start and end times. The algorithm calculates the minimum number of rooms (or groups) required, with each group representing a separate meeting room. This approach helps optimize room allocation and prevents scheduling conflicts.

### Steps to Implement the Solution

1. **List Meetings**: Gather all meetings with their respective start and end times.
2. **Create Time Points**: For each meeting, note down:
   - Start time
   - End time
3. **Sort Time Points**: Arrange all time points in chronological order. If two events occur at the same time, prioritize the end time.
4. **Count Overlaps**: Traverse through the sorted list and maintain a count of active meetings:
   - Increase the count at start times.
   - Decrease the count at end times.
5. **Determine Maximum Count**: The highest count reached during this process indicates the minimum number of rooms needed.

## Impact

Implementing this solution ensures:
- **Efficient Room Usage**: Maximizes the use of available meeting rooms.
- **Reduced Wasted Space**: Minimizes instances where rooms are left unused.
- **No Double-Booking**: Guarantees that meetings do not overlap in the same room.

## Example

Consider the following meetings:

- Meeting 1: 9 AM to 10 AM
- Meeting 2: 9:30 AM to 11 AM
- Meeting 3: 10 AM to 11:30 AM
- Meeting 4: 11 AM to 12 PM

### Calculation Steps:

1. **Time Points**:
   - Start: 9 AM, 9:30 AM, 10 AM, 11 AM
   - End: 10 AM, 11 AM, 11:30 AM, 12 PM
2. **Sorted Time Points**:
   - 9 AM (start)
   - 9:30 AM (start)
   - 10 AM (end)
   - 11 AM (start)
   - 11 AM (end)
   - 11:30 AM (end)
   - 12 PM (end)
3. **Counting Overlaps**:
   - At each time point, adjust the count based on whether it’s a start or end time.

### Result:

The maximum number of rooms needed for this example is **2**.

## Conclusion

By following this method, you can efficiently determine how many meeting rooms are necessary for any given schedule. This ensures smooth operations and optimal use of resources.
