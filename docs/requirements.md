# WeatherCheck — Software Requirements Specification

## 1. Introduction

### 1.1 Purpose
This document defines the functional and nonfunctional requirements for WeatherCheck. It establishes the expected application behavior and provides a basis for system design, implementation, and testing.

### 1.2 Project Overview
WeatherCheck is a cloud-hosted full-stack weather application that allows users to search for locations and view current weather conditions and short-term forecasts. The application uses a React frontend, Node.js backend, and external weather API without requiring user accounts or persistent storage.

For additional information about the project's goals, scope, and constraints, see [Project Definition](project-definition.md).

## 2. Functional Requirements

### 2.1 Location Search
- **FR-001:** The application shall allow users to search for locations by name.
- **FR-002:** The application shall display matching locations for users to select.
- **FR-003:** The application shall notify users when no matching locations are found.

### 2.2 Weather Information
- **FR-004:** The application backend shall retrieve weather information for a selected location from an external weather API.
- **FR-005:** The application shall display current temperature, weather conditions, humidity, and wind speed.
- **FR-006:** The application shall display a short-term weather forecast for the selected location.
- **FR-007:** The application shall notify users when weather information cannot be retrieved.

### 2.3 Application Behavior
- **FR-008:** The application shall allow users to search for another location without reloading the page.
- **FR-009:** The application shall display a loading indicator while weather information is being retrieved.
- **FR-010:** The application shall allow users to retry after a failed weather request.

## 3. Nonfunctional Requirements

### 3.1 Usability
- **NFR-001:** The application shall provide a responsive interface usable on desktop and mobile browsers.
- **NFR-002:** Weather information, navigation, and error messages shall be clearly presented.

### 3.2 Reliability
- **NFR-003:** The application shall handle failed API requests without crashing or becoming unusable.
- **NFR-004:** The application shall validate required search inputs and handle unexpected API responses.

### 3.3 Security
- **NFR-005:** Any required API credentials shall be stored securely and excluded from the public source code.
- **NFR-006:** The publicly hosted application shall use HTTPS.

### 3.4 Deployment
- **NFR-007:** The application shall support local development and public cloud deployment.
- **NFR-008:** Updates merged into the designated production branch shall trigger automatic deployment.
- **NFR-009:** The application shall provide documented setup and deployment instructions.

### 3.5 Maintainability
- **NFR-010:** The application shall maintain a clear separation between frontend and backend responsibilities.
- **NFR-011:** Automated tests shall verify essential functionality and error handling.

## 4. User Stories

- **US-001:** As a user, I want to search for a location so that I can find its weather information.
- **US-002:** As a user, I want to select a matching location so that I can retrieve weather information for the correct place.
- **US-003:** As a user, I want to view current weather conditions so that I can understand the weather at my selected location.
- **US-004:** As a user, I want to view a short-term forecast so that I can plan for upcoming weather.
- **US-005:** As a user, I want clear feedback when a search or weather request fails so that I understand what happened and can try again.
- **US-006:** As a user, I want to access WeatherCheck on desktop and mobile browsers so that I can use it on different devices.

## 5. Acceptance Criteria

### AC-001: Location Search (FR-001–FR-003)
- Users can enter a location name and submit a search.
- Matching locations are displayed when available.
- A clear message is displayed when no matches are found.
- Empty searches are handled without unnecessary API requests.

### AC-002: Current Weather (FR-004–FR-005)
- Selecting a location triggers a request through the application backend.
- Current temperature, conditions, humidity, and wind speed are displayed when available.
- Weather information corresponds to the selected location.

### AC-003: Weather Forecast (FR-006)
- A short-term forecast is displayed for the selected location.
- Forecast information includes the date, predicted temperature, and weather conditions.

### AC-004: Application Behavior (FR-007–FR-010)
- A loading indicator appears during weather requests.
- Users can search for another location without reloading the page.
- Failed requests produce a clear error message.
- Users can retry a failed request.

### AC-005: Interface and Reliability (NFR-001–NFR-004)
- The interface remains usable on desktop and mobile browser sizes.
- Invalid inputs and unexpected API responses do not cause the application to crash.
- Weather information and error messages remain readable.

### AC-006: Security and Deployment (NFR-005–NFR-009)
- Required API credentials are not exposed in the public repository or frontend.
- The deployed application is accessible through HTTPS.
- The application runs successfully in local and public environments.
- Merging a valid update into the production branch triggers deployment.
- Setup and deployment instructions are documented.

### AC-007: Maintainability and Testing (NFR-010–NFR-011)
- Frontend and backend responsibilities are separated.
- Automated tests cover the essential weather functionality and error handling.
- Automated tests pass before final project completion.

## 6. Assumptions and Dependencies

### Assumptions
- Users have internet access and a modern web browser.
- The selected weather API supports location search, current weather conditions, and short-term forecasts, either directly or through compatible endpoints.
- The application does not require user accounts, a database, or persistent user data.
- Weather information is provided by an external service rather than generated by WeatherCheck.

### Dependencies
- A third-party weather API for location and weather information.
- React for frontend development.
- Node.js for backend development.
- Git and GitHub for version control.
- Jira for project management.
- A cloud hosting provider supporting the application's deployment requirements.