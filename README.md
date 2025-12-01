# SOLID API in Node.js

An API for a GymPass-style application developed in Node.js using TypeScript, Fastify, and Prisma, following SOLID principles for clean, scalable, and maintainable code.

## Main Features of the Application

- **Users:** Can register, authenticate, and view their profiles.
- **Gyms:** Can be registered and searched by name or proximity.
- **Check-ins:** Users can check in at gyms, with business rules such as distance validation and daily check-in limits.

## Technologies Used

- **Node.js:** JavaScript runtime for server-side execution.
- **TypeScript:** JavaScript superset that adds static typing.
- **Fastify:** Web framework focused on performance and low overhead.
- **Prisma:** ORM for Node.js and TypeScript used to communicate with the PostgreSQL database.
- **Zod:** Schema and type validation library.
- **Vitest:** Testing framework for Vite-based (and Node.js) projects.
- **Docker:** Used to create a development environment with PostgreSQL.
- **TSX:** Runs TypeScript files directly without prior compilation in development.
- **TSUP:** Bundler for TypeScript libraries.

## Functional Requirements (FRs)

- [x] User registration must be possible;
- [x] User authentication must be possible;
- [x] It must be possible to retrieve the logged-in user's profile;
- [x] It must be possible to retrieve the number of check-ins performed by the logged-in user;
- [x] It must be possible for the user to retrieve their check-in history;
- [x] Users must be able to search for nearby gyms (within 10 km);
- [x] Users must be able to search for gyms by name;
- [x] Users must be able to check in at a gym;
- [x] It must be possible to validate a user’s check-in;
- [x] It must be possible to register a gym;

## Business Rules (BRs)

- [x] Users must not be able to register with a duplicate email;
- [x] Users cannot perform two check-ins on the same day;
- [x] Users cannot check in if they are not close to the gym (100m radius);
- [x] Check-ins can only be validated within 20 minutes of creation;
- [x] Check-ins can only be validated by administrators;
- [x] Gyms can only be registered by administrators;

## Non-Functional Requirements (NFRs)

- [x] User passwords must be encrypted;
- [x] Application data must be persisted in a PostgreSQL database;
- [x] All data lists must be paginated with 20 items per page;
- [x] Users must be identified using a JWT (JSON Web Token);
