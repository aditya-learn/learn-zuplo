# Zuplo API Specification

## Overview

The Zuplo API allows users to interact with various functionalities of the system. Below is a summary of the available endpoints and their corresponding operations.

## Endpoints

### /todos

- **Summary:** Get all todos API
- **Description:** First GET API on Zuplo
- **Route Configuration:**
  - **CORS Policy:** none
  - **Handler:**
    - **Export:** urlForwardHandler
    - **Module:** `$import(@zuplo/runtime)`
    - **Options:**
      - `baseUrl`: `${env.BASE_URL}`
  - **Policies:**
    - **Inbound:**
      - api-key-inbound
      - rate-limit-inbound
      - set-headers-inbound
- **Operation ID:** b82cf4bc-94dd-495d-b945-fcecb0bad38e
- **Internal:** false

## TypeScript Interface

```typescript
export type Root = Root2[];

export interface Root2 {
  userId: number;
  id: number;
  title: string;
  completed: boolean;
}
