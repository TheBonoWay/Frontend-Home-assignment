# Frontend Home Assignment
Front-end Developer Home Assignment - July 2024

# Bono Nonprofit Portfolio Builder

This project is a front-end developer assignment for Bono, built using Next.js. It consists of a flow of three screens using an existing backend API to build a nonprofit portfolio. The project focuses on working with APIs, SEO, server-side rendering, and code quality.

## Features

- **API Interaction**: Interact with the Bono API to fetch and display causes.
- **SEO**: Include proper meta tags and Open Graph tags for SEO.
- **Server-Side Rendering**: Utilize Next.js's server-side rendering capabilities.
- **Responsive Design**: Ensure the project is responsive and works well on various screen sizes.

## API

This project uses the Bono API to fetch causes.
- **Endpoint**: `https://dev.api.bono.so/v1`
- **Documentation**: [API Documentation](https://dev.api.bono.so/v1/swagger#/)

## Screens
The project screens are designed and available in our production system: [Bono](https://app.bono.so).
Please note that the flow in this assignment is different from the production system.

### 1. Welcome Screen
![Welcome Screen](/screens/01_welcome/Frame.png)

This is the first screen that the user sees. The design is provided in the `screens` folder.
- Link the Terms and Conditions and Privacy Policy to the respective marketing site pages.
- On clicking 'Let's Start', navigate the user to the Cause Selection screen.

### 2. Cause Selection Screen
![Cause Screen](/screens/02_causes/empty.png)

The purpose of this screen is to let the user select 3 causes and view details about them.
- Users cannot select fewer or more than 3 causes.
- Use the API endpoint `/v1/charity/causes` to fetch the causes. No authentication is required.
- Display cause details and an image when the user clicks on a cause.
- Ensure the mobile design includes a scroller showing only 2 rows.
- The API will always return 9 causes.

After the user completes the selection, navigate to the Signup screen.

### 3. Signup Screen
![Signup Screen](/screens/03_signup/iPhone%2013%20mini%20-%20172.png)

Replicate the design as shown in the image.
- No need to implement Google login functionality; only create the design.
- On form submission, send the data to `/v1/auth/register/anonymous`.
- Include the selected causes' IDs in the payload.
- POST payload example:
```json
{
  "email": "string@test.com",
  "firstName": "string",
  "causes": [1, 2, 3]
}
