<%*
const name = await tp.system.prompt("Location name");
await tp.file.rename(name);
tR += `---
type: location
tags:
  - location
---

# ${name}

## At a glance
- **Kind:**
- **Description:**
- **Current situation:**

## Run the scene
- **What stands out:**
- **Useful features / hazards:**
- **Scene hook:**

## Connections
- **People:**
- **Nearby places:**
- **Secrets:**
`;
%>
