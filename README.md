# Workout Plan API Documentation
workout_plan api using express

## Overview
The **Workout Plan API** allows users to retrieve workout routines based on the day of the week. This API is built using Express.js and serves data from a JSON file (`index.json`).

### Base URL
```
https://workout-plan-api.onrender.com
```

## Endpoints

### 1. Get All Workout Plans
**Endpoint:**
```
GET [YOUR_DEPLOYED_API_URL]/workout_plan
```
**Description:**
Fetches the entire workout plan.

**Response:**
```json
{
  "status": 200,
  "msg": "successfully read",
  "data": [
    {
      "day": "Monday",
      "exercise": "Chest & Triceps",
      "workouts": [
        { "name": "Bench Press", "sets": 4, "reps": 10 },
        { "name": "Incline Dumbbell Press", "sets": 3, "reps": 12 },
        { "name": "Tricep Dips", "sets": 3, "reps": 12 }
      ]
    },
    ...
  ]
}
```

### 2. Get Workout Plan by Day
**Endpoint:**
```
GET [YOUR_DEPLOYED_API_URL]/workout_plan/:day
```
**Description:**
Fetches workout routines for a specific day.

**Example Request:**
```
GET [YOUR_DEPLOYED_API_URL]/workout_plan/Monday
```

**Response:**
```json
{
  "msg": "successfully sent",
  "status": 200,
  "data": [
    {
      "day": "Monday",
      "exercise": "Chest & Triceps",
      "workouts": [
        { "name": "Bench Press", "sets": 4, "reps": 10 },
        { "name": "Incline Dumbbell Press", "sets": 3, "reps": 12 },
        { "name": "Tricep Dips", "sets": 3, "reps": 12 }
      ]
    }
  ]
}
```

## How to Use the API

### 1. Accessing the API
- Open a web browser or use Postman to make a `GET` request.
- Use the base URL `[YOUR_DEPLOYED_API_URL]` to access the endpoints.

### 2. Example Requests
- Get the full workout plan: `[YOUR_DEPLOYED_API_URL]/workout_plan`
- Get workout for a specific day: `[YOUR_DEPLOYED_API_URL]/workout_plan/Tuesday`

### 3. Testing with cURL
```sh
curl -X GET [YOUR_DEPLOYED_API_URL]/workout_plan
```

```sh
curl -X GET [YOUR_DEPLOYED_API_URL]/workout_plan/Wednesday
```

## Conclusion
This API provides a simple way to retrieve structured workout plans. Replace `[YOUR_DEPLOYED_API_URL]` with your actual deployment URL to use it live.

