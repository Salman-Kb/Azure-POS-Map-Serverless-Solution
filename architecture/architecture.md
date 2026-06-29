# Architecture Overview

## Workflow

1. Employee uploads Excel file.
2. Blob Storage receives file.
3. Blob Trigger activates Azure Function.
4. Function validates data.
5. Function generates JSON.
6. JSON is stored in Static Website storage.
7. Website reads JSON dynamically.
8. Users see latest POS data.

## Design Decisions

### Why Azure Functions

- Event-driven
- Cost-effective
- No servers to manage

### Why JSON

- Fast loading
- Easier frontend integration

### Why Static Website

- Simple hosting
- Low cost
- Highly scalable
