# ✨ 👨‍🚀 XeCaps - Space Mission Control Backend 👩‍🚀 ✨

This is a **TypeScript/Express** backend for managing space mission planning, including:
- user authentication
- mission management
- astronaut allocation
- launch vehicle management
- launch state transitions
- payload deployment
- LLM-powered astronaut chat

---

## Features

- User authentication and session management
- Mission CRUD operations with ownership validation
- Astronaut pool management and mission assignment
- Launch vehicle creation, update, retirement, and launch allocation
- Launch lifecycle simulation using state transitions
- Payload deployment tracking
- LLM-backed astronaut chat using OpenRouter API
- REST API documentation via Swagger
- HTTP-level tests with Jest

---

## Tech Stack

- TypeScript
- Node.js / Express
- Jest / ts-jest
- Swagger UI
- JSON-file persistence
- OpenRouter API

---

## Architecture

```txt
src/
├── server.ts          # Express routes and HTTP layer
├── auth.ts            # Authentication and session logic
├── mission.ts         # Mission management
├── astronaut.ts       # Astronaut management and LLM chat
├── launch.ts          # Launch lifecycle and payload logic
├── launchVehicle.ts   # Launch vehicle management
├── dataStore.ts       # JSON-backed data persistence
└── helpers.ts         # Shared validation and utility functions
```

---

## Getting Started

```bash
npm install
cp .env.example .env.local
num run start-dev
```
Then open:
```
http://127.0.0.1:3200/docs
```

### Environment Variables

Please fill in your own openrouter api key in `.env.local`. You can refer to the example in `.env.example`:
```env
OPENROUTER_API_KEY=
```

---

## Testing

```bash
npm run lint
npm run tsc
npm test
```

---

## My Contributions

- Implemented **core admin-side** backend features, including `adminAuthRegister`, `adminMissionInfo`, `adminAstronautAssign`, and `adminAstronautUnassign`.
- Built the corresponding **API/interface layer** for these features, ensuring that backend logic could be accessed through the project’s request/response structure.
- Wrote **tests** for the implemented admin authentication, mission information, astronaut assignment, and astronaut unassignment behaviours.
- Implemented `launchVehicleList`, supporting retrieval of launch vehicle information within the project’s launch management workflow.
- Designed most of the project’s **core data types and data structures**, covering admins, missions, astronauts, launches, launch vehicles, and related system state.

---

## Course Context and Attribution

This project was This project was originally developed as a group backend project for UNSW College DPST1093. The public version has been cleaned and reorganised for portfolio use after the course project changed. Course-provided starter/adaptation code is either removed or clearly separated from implemented project code.

### Original Team

| Member | Main Contributions |
| ------ | ------------------ |
| Yulin Guo / Alan | ... |
| Xiangting Li / Chris | Admin registration, mission information, astronaut assignment/unassignment, launchVehicle list, corresponding API interface layer, tests, core data structure design |
| Yuchen Wang / Eric | ... |
| You Wu / William | ... |
| Zhen Cao / Zhen | ... |