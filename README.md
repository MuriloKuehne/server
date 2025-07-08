# NLW Agents Server

This is the backend server for the NLW Agents application, built with Node.js, Fastify, and PostgreSQL.

## Technologies Used

- **Node.js**: JavaScript runtime environment
- **Fastify**: Fast and low overhead web framework
- **PostgreSQL**: Powerful, open-source object-relational database system
- **Drizzle ORM**: TypeScript ORM for SQL databases
- **Zod**: TypeScript-first schema declaration and validation library
- **TypeScript**: Typed superset of JavaScript
- **Biome**: Linter, formatter, and more for web development

## Project Structure

The project follows a modular structure, with a clear separation of concerns:

```
├── src/
│   ├── db/
│   │   ├── migrations/
│   │   ├── schema/
│   │   ├── connection.ts
│   │   └── seed.ts
│   ├── http/
│   │   └── routes/
│   ├── env.ts
│   └── server.ts
```

- **`src/db`**: Contains all database-related files, including the connection setup, schema definitions, migrations, and seed scripts.
- **`src/http`**: Holds the HTTP server logic, including routes and handlers.
- **`src/env.ts`**: Manages environment variables using Zod for validation.
- **`src/server.ts`**: The entry point of the application, where the Fastify server is initialized.

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/en/) (v20 or higher)
- [Docker](https://www.docker.com/) (for running PostgreSQL)

### Installation and Setup

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your-username/your-repository.git
   cd your-repository
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Set up the environment variables:**

   Create a `.env` file in the root of the project by copying the `.env.example` file:

   ```bash
   cp .env.example .env
   ```

   Update the `.env` file with your PostgreSQL database credentials.

4. **Start the PostgreSQL database using Docker:**

   ```bash
   docker-compose up -d
   ```

5. **Run the database migrations:**

   This will create the necessary tables in your database.

   ```bash
   npm run db:migrate
   ```

6. **Seed the database (optional):**

   This will populate the database with initial data.

   ```bash
   npm run db:seed
   ```

7. **Start the development server:**

   ```bash
   npm run dev
   ```

The server will be running at `http://localhost:3333`.
