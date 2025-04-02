# **System Design: Habit Tracker App**

## **1. System Architecture**

### **1.1 High-Level Architecture**

The Habit Tracker App will be built using **Firebase (Free Tier)** as the backend and **vanilla JavaScript** for both frontend and backend development (without React, Node.js, or any other framework).

#### **Components:**

- **Frontend**: Vanilla JavaScript, HTML, CSS (No frameworks used)
    
- **Backend**: Firebase (No Node.js or Cloud Functions used)
    
- **Database**: Firestore (NoSQL Database, limited reads/writes per day)
    
- **Authentication & Authorization**: Firebase Authentication (Email/Password, Google Sign-In, etc.)
    
- **Storage**: Firebase Storage (Only for essential files, avoiding high bandwidth usage)
    
- **Notifications**: Firebase Cloud Messaging (Limited quota for free tier)
    
- **Analytics**: Firebase Analytics (Basic insights, avoiding real-time heavy tracking)
    
- **Hosting**: Firebase Hosting (Optimized for static assets)
    

## **2. Database Design**

### **2.1 Firestore Data Structure (Optimized for Free Tier)**

Firestore follows a **document-based NoSQL structure** with minimal reads/writes.

#### **Users Collection**

```
users (Collection)
  ├── {userId} (Document)
      ├── name: String
      ├── email: String
      ├── createdAt: Timestamp
```

#### **Habits Collection**

```
habits (Collection)
  ├── {habitId} (Document)
      ├── userId: String (Reference to Users)
      ├── name: String
      ├── category: String
      ├── frequency: Object (daily, weekly, etc.)
      ├── difficulty: String (Easy, Medium, Hard)
      ├── createdAt: Timestamp
```

#### **Habit Tracking Collection**

```
habit_tracking (Collection)
  ├── {logId} (Document)
      ├── userId: String (Reference to Users)
      ├── habitId: String (Reference to Habits)
      ├── status: String (Completed, Missed, Skipped)
      ├── timestamp: Timestamp
```

#### **Achievements Collection**

```
achievements (Collection)
  ├── {achievementId} (Document)
      ├── userId: String (Reference to Users)
      ├── habitId: String (Reference to Habits)
      ├── milestone: String
      ├── earnedAt: Timestamp
```

## **3. Frontend Implementation with Vanilla JavaScript**

### **3.1 File Structure**

```
/public
  ├── index.html  # Main HTML file
  ├── styles.css  # Stylesheet
  ├── app.js  # Core JavaScript logic
  ├── firebase-config.js  # Firebase initialization
```

### **3.2 Core Functionalities**

- **User authentication (Sign Up, Login, Logout) using Firebase Auth**
    
- **CRUD operations for habits using Firestore**
    
- **Habit tracking and streak calculation**
    
- **Basic progress reports using Firebase queries**
    
- **Reminder notifications using Firebase Cloud Messaging**
    
- **Minimal UI using HTML, CSS, and JavaScript DOM manipulation**
    

## **4. Scalability & Performance Considerations (Optimized for Free Firebase Tier)**

### **4.1 Firestore Optimization**

- **Minimize Reads/Writes**: Use batched writes and cache user data locally.
    
- **Indexed Queries**: Avoid complex queries that increase read operations.
    
- **Denormalization**: Store frequently accessed data in documents to reduce nested lookups.
    

### **4.2 Caching & Performance Enhancements**

- **Firestore Offline Mode**: Store user data locally to minimize reads.
    
- **Lazy Loading**: Load data incrementally instead of fetching large datasets.
    

## **5. Security & Compliance**

- **Firebase Security Rules** to restrict access based on user authentication.
    
- **OAuth2 / JWT** authentication for secure API access.
    
- **GDPR Compliance**: Users can request data deletion.
    

## **6. DevOps & Deployment (Optimized for Firebase Free Tier)**

### **6.1 CI/CD Pipeline**

- **GitHub Actions** for automated deployments with Firebase CLI.
    
- **Firebase Hosting** for lightweight deployment.
    

### **6.2 Logging & Monitoring**

- **Firebase Crashlytics** for monitoring app performance (Basic free-tier monitoring).
    
- **Firebase Analytics** for tracking user interactions (Limited event tracking).
    

## **Conclusion**

This system design ensures the **Habit Tracker App** is optimized for Firebase's **Free Tier**, balancing **performance, efficiency, and cost-effectiveness** while using **pure JavaScript (no frameworks, no Node.js).**