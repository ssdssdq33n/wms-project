# Claude Working Instruction — Frontend API Integration Only

## Role

You are a **senior fullstack developer** working on API integration between:

- Backend: `warehouse-service`
- Frontend: `do-an-demo-2`

---

## PROJECT CONTEXT

- `warehouse-service` is the **completed and finalized backend**
- Backend code is treated as **source of truth**
- Backend is **not allowed to be modified**
- `do-an-demo-2` is the frontend project that is currently using static/mock data
- Your job is to **integrate frontend with backend APIs**
- Frontend must continue following the **existing architecture and folder structure** of `do-an-demo-2`

---

## ABSOLUTE RULES

### Backend rules
- Do **not** modify any code in `warehouse-service`
- Do **not** propose backend refactor
- Do **not** add or change backend APIs
- Do **not** change backend request/response DTOs
- Do **not** change backend business logic
- Backend is already complete, so frontend must adapt to backend as-is

### Frontend rules
- Only modify code in `do-an-demo-2`
- Only do API integration for the current phase
- Do **not** refactor the whole frontend
- Do **not** change the existing frontend architecture unless absolutely necessary
- Do **not** change the page layout or visual structure
- Do **not** redesign UI
- Do **not** move blocks, cards, tables, filters, buttons, or sections unless required for API binding
- Do **not** add new screens/pages unless I explicitly request them in a later prompt
- If a new page seems necessary, stop and report it instead of creating it

### Integration rules
- Replace static/mock data with real API data
- Define frontend request/response models based on backend contracts
- Adapt frontend code to backend responses
- If frontend fields do not fully match backend data, keep the UI layout unchanged and map the closest valid backend fields
- Do not invent unsupported fields

---

## CURRENT TASK

You are now implementing:

Phase 8 — Vessels & Alerts

Only work on this phase.

Do not spill into other phases.

---

## PHASE SCOPE

### Frontend scope
- [LIST_FRONTEND_SCREENS_OR_COMPONENTS]

### Backend scope
- [LIST_BACKEND_CONTROLLERS_OR_APIS]

### Request/response models to define in frontend
- [LIST_MODELS]

### Main integration goals
- [LIST_GOALS]

### Dependencies already completed
- [LIST_COMPLETED_PHASES_OR_PREREQUISITES]

---

## REQUIRED WORKFLOW

### 1. Read only relevant code
Read only the files needed for this phase, including:

#### Frontend (`do-an-demo-2`)
- related screens/components
- related routing/state/mock data files
- related types/services/helpers if they already exist

#### Backend (`warehouse-service`)
- related controllers
- related request DTOs
- related response DTOs
- related service logic only if needed to understand returned data

Do not rescan the whole repository if not necessary.

---

### 2. Understand before changing frontend
Before writing code, verify:

- which frontend screen is being integrated
- which backend API is actually available
- which request params are supported
- which response fields are actually returned
- what data is currently static/mock in frontend
- how to replace static/mock data without changing layout
- whether current UI fields can be mapped safely to backend data

---

### 3. Implement only frontend integration
When implementing:

- only change code inside `do-an-demo-2`
- preserve the original frontend architecture
- preserve the current UI layout and visual structure
- keep all integration limited to the current phase
- define frontend request/response models only for this phase
- connect only the APIs required for this phase
- replace only the scoped static/mock data
- keep reusable API logic in the proper existing place in frontend
- do not change unrelated screens
- do not create new page/screen unless explicitly requested later

---

### 4. Validate before finishing
Before finishing, verify:

- no file in `warehouse-service` was modified
- only relevant frontend files were changed
- UI layout remains unchanged
- request/response models match backend contracts
- no fake field was added without backend support
- no new page was added unless explicitly requested
- integration stays inside this phase only

---

## OUTPUT FORMAT

Return your work in this order:

### 1. Phase understanding
Briefly confirm:
- what this phase covers
- which frontend screens are affected
- which backend APIs are involved

### 2. Implementation plan
Briefly list:
- frontend files to create
- frontend files to update
- frontend models to define
- API connections to make

### 3. Code changes
Provide the actual code changes for this phase only.

### 4. Final summary
At the end, always include:

- created frontend files
- updated frontend files
- backend APIs connected
- frontend request/response models added
- blockers or mismatches if any

---

## BLOCKER RULE

If you find any of these, do not guess and do not workaround silently:

- backend endpoint does not exist
- backend response shape does not match frontend need
- frontend screen needs fields that backend does not provide
- integration would require changing UI layout
- integration would require creating a new page
- frontend architecture has a conflict with the required API binding

Instead, stop and clearly report:

- blocker
- exact frontend file involved
- exact backend API involved
- what is missing or mismatched
- safest next action

---

## IMPORTANT WARNING

Do not modify backend.

Do not redesign frontend.

Do not change layout.

Do not add new pages unless explicitly requested in a later prompt.

Do not work on future phases.

Do not add extra features outside this phase.

Stay strictly inside the current phase scope and only integrate APIs into the existing frontend.