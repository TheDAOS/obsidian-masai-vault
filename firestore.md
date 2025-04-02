To create a Firebase Firestore database for the Habit Tracker App, you need to define the data structure that will support all the features mentioned. Below is a detailed schema for the Firestore database, including collections and documents that will store user data, habits, progress, and other relevant information.

### Firestore Database Schema

#### Collections and Documents

1. **Users**
   - **Document ID**: User ID (e.g., `user123`)
   - **Fields**:
     - `name`: String
     - `email`: String
     - `createdAt`: Timestamp
     - `lastLogin`: Timestamp
     - `habits`: Array of habit IDs (references to the `Habits` collection)

2. **Habits**
   - **Document ID**: Habit ID (e.g., `habit123`)
   - **Fields**:
     - `userId`: String (reference to the `Users` collection)
     - `name`: String
     - `description`: String
     - `category`: String (e.g., "Health", "Personal Development")
     - `type`: String (e.g., "daily", "weekly")
     - `difficulty`: String (e.g., "easy", "moderate", "hard")
     - `createdAt`: Timestamp
     - `lastUpdated`: Timestamp
     - `streak`: Number
     - `totalCompleted`: Number
     - `goal`: Number (e.g., total miles to run in a month)
     - `reminders`: Array of reminder objects
       - `time`: String (e.g., "08:00")
       - `days`: Array of days (e.g., ["Monday", "Wednesday", "Friday"])

3. **HabitLogs**
   - **Document ID**: Log ID (e.g., `log123`)
   - **Fields**:
     - `habitId`: String (reference to the `Habits` collection)
     - `userId`: String (reference to the `Users` collection)
     - `date`: Timestamp
     - `completed`: Boolean
     - `duration`: Number (in minutes)
     - `notes`: String

4. **Achievements**
   - **Document ID**: Achievement ID (e.g., `achievement123`)
   - **Fields**:
     - `userId`: String (reference to the `Users` collection)
     - `name`: String
     - `description`: String
     - `dateEarned`: Timestamp
     - `habitId`: String (reference to the `Habits` collection)

5. **Challenges**
   - **Document ID**: Challenge ID (e.g., `challenge123`)
   - **Fields**:
     - `name`: String
     - `description`: String
     - `startDate`: Timestamp
     - `endDate`: Timestamp
     - `participants`: Array of user IDs (references to the `Users` collection)
     - `habitId`: String (reference to the `Habits` collection)

6. **Reports**
   - **Document ID**: Report ID (e.g., `report123`)
   - **Fields**:
     - `userId`: String (reference to the `Users` collection)
     - `period`: String (e.g., "weekly", "monthly")
     - `startDate`: Timestamp
     - `endDate`: Timestamp
     - `data`: Object (contains summary statistics and insights)

### Example Data

#### Users Collection
```json
{
  "user123": {
    "name": "Sam",
    "email": "sam@example.com",
    "createdAt": "2023-10-01T00:00:00Z",
    "lastLogin": "2023-10-05T08:30:00Z",
    "habits": ["habit123", "habit124"]
  }
}
```

#### Habits Collection
```json
{
  "habit123": {
    "userId": "user123",
    "name": "Exercise",
    "description": "Daily workout routine",
    "category": "Fitness",
    "type": "daily",
    "difficulty": "moderate",
    "createdAt": "2023-10-01T00:00:00Z",
    "lastUpdated": "2023-10-05T08:30:00Z",
    "streak": 5,
    "totalCompleted": 15,
    "goal": 30,
    "reminders": [
      {
        "time": "07:00",
        "days