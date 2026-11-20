# Online Canteen Food-Ordering System

## Student Details

-   **Name:** \[\Sohan Rao\]
-   **USN:** \[NB25CSE354\]
-   **Assigned Case Study:** Question 2 -- Mobile and Web Applications
    Engineering

------------------------------------------------------------------------

## 1. Introduction

Mobile and web applications allow users to access digital services
through smartphones, tablets, and computers. A mobile application is
installed on a device, while a web application is accessed through a web
browser. A Progressive Web Application (PWA) is a web application that
uses modern browser technologies to provide an app-like experience,
including installation on supported devices.

For a college canteen, an online food-ordering system can help students
view available food, place orders, pay online, and receive notifications
when their orders are ready. It can reduce queues, make ordering more
convenient, and help canteen staff manage orders efficiently.

## 2. Problem Analysis

In a traditional college canteen, students may have to stand in queues
to check the menu, place orders, and make payments. During busy hours,
this can lead to long waiting times, crowding, order confusion, and
difficulty tracking whether food is ready.

The proposed system should provide a convenient way for students to
order food before reaching the counter. Canteen staff should also be
able to view incoming orders and update their status.

## 3. Comparison of Mobile, Web, and Progressive Web Applications

  ------------------------------------------------------------------------
  Approach          Description       Advantages        Limitations
  ----------------- ----------------- ----------------- ------------------
  Mobile            An application    App-like          Users may need to
  application       installed from an experience,       install it;
                    app store or      device            separate Android
                    distributed       integration, and  and iOS
                    directly to a     support for push  development can
                    device.           notifications.    increase effort.

  Web application   A system accessed No installation   Some device
                    through a browser required, easy to features and
                    using a URL.      update, and       background
                                      accessible across capabilities may
                                      devices with a    be more limited;
                                      compatible        internet access is
                                      browser.          generally
                                                        required.

  Progressive Web   A web application Can be installed  Browser and
  Application (PWA) enhanced with     on supported      operating-system
                    technologies such devices, works    support varies;
                    as a web app      across many       some capabilities
                    manifest and      platforms, and    may differ by
                    service workers.  can support       device.
                                      selected offline  
                                      features and      
                                      notifications     
                                      where supported.  
  ------------------------------------------------------------------------

## 4. Selection of a Suitable Application Type

A **Progressive Web Application (PWA)** is a suitable choice for the
college canteen food-ordering system.

A PWA can be opened through a link without requiring students to
download an application from an app store. Students can also add it to
their device's home screen on supported platforms for quicker access. A
single responsive application can serve students using smartphones,
tablets, or computers.

This approach is suitable for a college environment because it can
reduce installation barriers and simplify updates. The college can
maintain one application that students access using a browser or an
installed PWA experience. The system should still require an internet
connection for live menu updates, order submission, payment processing,
and current order status.

## 5. Major Functionalities

### 5.1 Menu Browsing

-   Display food items with names, descriptions, prices, and
    availability.
-   Organize items into categories such as snacks, meals, and beverages.
-   Show unavailable items clearly.
-   Allow students to view the menu before placing an order.

### 5.2 Order Placement and Tracking

-   Allow students to select food items and specify quantities.
-   Display an order summary and total amount before confirmation.
-   Generate a unique order number after successful submission.
-   Allow students to view order progress, such as **Placed**,
    **Preparing**, and **Ready for Collection**.

### 5.3 Online Payment

-   Show the total amount before payment.
-   Integrate a secure payment gateway for supported payment methods.
-   Display payment success or failure status.
-   Maintain a transaction reference for the order and avoid treating an
    unsuccessful payment as a completed payment.

### 5.4 Notifications

-   Notify students when an order is accepted and when it is ready for
    collection.
-   Show order updates within the application.
-   Use browser or device push notifications where supported and where
    the student has granted permission.
-   Provide an in-app status view as an alternative if push
    notifications are unavailable.

## 6. Development Challenges

### 6.1 Payment Security and Reliability

The system must protect payment-related information and communicate
securely with the payment gateway. It must handle failed, delayed, or
duplicate payment responses correctly. Using a trusted payment provider
and secure communication (HTTPS) can help address these concerns.

### 6.2 Real-Time Order Updates

Students need accurate information about whether their orders are being
prepared or are ready. Delayed or incorrect updates can cause confusion.
The application should provide a reliable way for canteen staff to
update order statuses and for students to refresh or receive those
updates.

### 6.3 Device and Browser Compatibility

Students may use different phones, screen sizes, browsers, and operating
systems. PWA installation and notification features may not behave
identically everywhere. The application should use responsive design and
be tested on commonly used devices and browsers, with an in-app
alternative for features that are not supported.

## 7. Simple Application Workflow Diagram

``` mermaid
flowchart TD
    A[Student opens the Canteen PWA] --> B[Browse food menu]
    B --> C[Select food items and quantities]
    C --> D[Review order and total]
    D --> E[Make online payment]
    E --> F{Payment successful?}
    F -- No --> G[Show payment failure and retry option]
    G --> E
    F -- Yes --> H[Send order to canteen]
    H --> I[Canteen staff prepare the order]
    I --> J[Staff update order status to Ready]
    J --> K[Notify student]
    K --> L[Student collects the order]
```

## 8. Benefits of the Proposed System

-   **Reduced waiting time:** Students can place orders before reaching
    the counter.
-   **Convenient access:** The PWA can be opened through a browser and
    installed on supported devices.
-   **Better order management:** Canteen staff can view and update
    incoming orders.
-   **Improved communication:** Order-status updates help students know
    when to collect their food.
-   **Simpler maintenance:** A single responsive PWA can serve users
    across multiple device types.

## 9. Conclusion

A Progressive Web Application is a practical choice for the proposed
college canteen food-ordering system. It combines the accessibility of a
web application with selected app-like features, while avoiding the need
for every student to install a separate native application. Menu
browsing, order placement and tracking, online payment, and
notifications are the main functionalities required. By addressing
payment security, reliable order updates, and device compatibility
during development, the college can provide students with a convenient
and efficient food-ordering service.

------------------------------------------------------------------------

**GitHub file name:** `USN_Canteen_Application.md`

**Submission reminder:** Replace the student-detail placeholders, save
this file inside the repository's `contributions` folder, commit it to
your fork, and submit a Pull Request to the faculty repository as
described in the activity instructions.

