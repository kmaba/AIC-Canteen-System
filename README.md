# AIC Canteen Order System

## Making Canteen Orders for Teachers Easier

### Intent

This project aims to simplify and streamline the process of making canteen orders for teachers at AIC.

If you are starting a Flutter project of your own, here are some resources to consider:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the [online documentation](https://docs.flutter.dev/), which offers tutorials, samples, guidance on mobile development, and a full API reference.

### Potential Struggles

I need to develop an app that includes the following features:

- [ ] **Secure System:** Ensure the application is secure and protects user data.
- [ ] **Restricted Access:** Only allow teachers with email addresses under the organization `@aic.wa.edu.au`.
- [ ] **Student Blacklist:** Prevent students from accessing the system by blocking email addresses with student ID numbers (e.g., `XXXXX@aic.wa.edu.au`).
- [ ] **Order Management Server:** Create a server to manage orders with functionalities such as deny, accept, order fulfilled, and 'On my way.'

---

## Implementation Plan

### Secure System
1. **Authentication:** Use Firebase Authentication to securely authenticate users.
2. **Data Encryption:** Ensure all sensitive data is encrypted both in transit and at rest.
3. **Access Control:** Implement role-based access control (RBAC) to restrict access to authorized users only.

### Restricted Access
1. **Email Verification:** Check the user's email domain during the sign-up process to ensure it matches `@aic.wa.edu.au`.
2. **Admin Approval:** Optionally, require an admin to approve new users before they can access the system.

### Student Blacklist
1. **Email Pattern Matching:** Implement email validation to reject any email addresses with the student ID pattern (`XXXXX@aic.wa.edu.au`).
2. **Database Check:** Cross-reference email addresses against a database of known student emails to ensure no students can access the system.

### Order Management Server
1. **Server Setup:** Set up a server using Node.js and Express to handle order management.
2. **Order APIs:** Create RESTful APIs to handle the following actions:
   - **Deny Order:** Allow admins to deny an order.
   - **Accept Order:** Allow admins to accept an order.
   - **Order Fulfilled:** Mark an order as fulfilled.
   - **On My Way:** Update the status of an order to 'On my way.'
3. **Database Integration:** Use a database (e.g., Firebase Firestore) to store and manage order data.
4. **Real-time Updates:** Implement real-time updates using WebSockets or Firebase Firestore to keep the client app in sync with the server.

---

### Resources and References

- **Flutter Documentation:** [Flutter Documentation](https://docs.flutter.dev/)
- **Firebase Documentation:** [Firebase Documentation](https://firebase.google.com/docs)
- **Node.js Documentation:** [Node.js Documentation](https://nodejs.org/en/docs/)
- **Express Documentation:** [Express Documentation](https://expressjs.com/en/starter/installing.html)

By following this plan and leveraging the provided resources, we can develop a secure, efficient, and user-friendly canteen order system for teachers at AIC.