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
GET https://workout-plan-api.onrender.com/workout_plan
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
GET https://workout-plan-api.onrender.com/workout_plan/:day
```
**Description:**
Fetches workout routines for a specific day.

**Example Request:**
```
GET https://workout-plan-api.onrender.com/workout_plan/Monday
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
- Use the base URL `https://workout-plan-api.onrender.com` to access the endpoints.

### 2. Example Requests
- Get the full workout plan: `https://workout-plan-api.onrender.com/workout_plan`
- Get workout for a specific day: `https://workout-plan-api.onrender.com/workout_plan/Tuesday`

### 3. Testing with cURL
```sh
curl -X GET https://workout-plan-api.onrender.com/workout_plan
```

```sh
curl -X GET https://workout-plan-api.onrender.com/workout_plan/Wednesday
```

## Conclusion
This API provides a simple way to retrieve structured workout plans `https://workout-plan-api.onrender.com/workout_plan`

