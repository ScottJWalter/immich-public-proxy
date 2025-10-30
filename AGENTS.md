# Agent Instructions for immich-public-proxy

## Build/Lint/Test Commands
- **Build**: `cd app && npm run build` (TypeScript → dist/)
- **Dev**: `cd app && npm run dev` (ts-node dev server)
- **Start**: `cd app && npm run start` (production server)
- **Test**: `cd app && npm run test` (Docker integration test)
- **Lint**: `cd app && npx eslint src/**/*.ts` (ESLint + TypeScript)
- **Type check**: `cd app && npx tsc --noEmit` (strict TypeScript)

## Code Style Guidelines
- **Imports**: ES6 imports, external libs first, relative paths from `src/`
- **Types**: Strict TypeScript (`noImplicitAny`, `strictNullChecks`), PascalCase types/interfaces/enums
- **Naming**: camelCase vars/functions, PascalCase types, `?` for optional interface props
- **Error Handling**: try/catch for failures, log with timestamps, appropriate HTTP codes
- **Formatting**: ESLint standard + TypeScript, JSDoc for exports, consistent spacing
- **Security**: Never log secrets, validate inputs, use crypto.randomBytes(), secure headers