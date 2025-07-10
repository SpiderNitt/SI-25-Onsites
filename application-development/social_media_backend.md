# Backend Infrastructure for Social Media Platform

## Objective

Design and implement a backend API for a basic social media platform focused on managing friend connections. This includes sending and managing friend requests, notifying users of pending requests, and retrieving friend statistics. The system should follow a modular backend structure with clearly separated concerns using `index.js/ts`, `routes`, `controllers`, and `models/schema`.

## Key Features to Implement

### 1. Sending Friend Requests

**Functionality:**  
Allow users to send friend requests to other users.

**Requirements:**
- `POST /friend-request/send`
- Validate if the request is not a duplicate or already accepted.
- Store the request in a pending state in the database.
- Notify the receiver (via stored notification or push system).

### 2. Accepting/Declining Friend Requests

**Functionality:**  
Allow users to respond to incoming friend requests.

**Requirements:**
- `POST /friend-request/respond`
- Request payload should include the request ID and action (accept/decline).
- On **accept**: Add each user to the other's friend list.
- On **decline**: Remove or mark the request as declined.

### 3. Notifications for Friend Requests

**Functionality:**  
Alert users when they receive new friend requests.

**Requirements:**
- `GET /notifications`
- Retrieve list of pending notifications (e.g., new friend requests).
- Store timestamps and optionally a read/unread state.

### 4. Fetching Friend Count

**Functionality:**  
Allow users to see how many friends they have.

**Requirements:**
- `GET /friends/count`
- Return the total number of confirmed (mutual) friends for the user.


