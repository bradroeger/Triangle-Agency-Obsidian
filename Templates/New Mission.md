<%*
const missionName = await tp.system.prompt("Mission name");

if (!missionName || !missionName.trim()) {
  tR += "Mission creation cancelled.";
} else {
  const name = missionName.trim();
  const folderName = name.replace(/[<>:"/\\|?*]/g, "-").replace(/[. ]+$/g, "") || "Untitled Mission";
  const missionFolder = `Missions/${folderName}`;
  const overviewPath = `${missionFolder}/Overview.md`;

  if (app.vault.getAbstractFileByPath(overviewPath)) {
    tR += `A mission overview already exists at ${overviewPath}. Choose a different mission name.`;
  } else {
    for (const folder of ["Missions", missionFolder, `${missionFolder}/Locations`, `${missionFolder}/Characters`, `${missionFolder}/Anomalies`]) {
      if (!app.vault.getAbstractFileByPath(folder)) await app.vault.createFolder(folder);
    }

    await tp.file.move(`${missionFolder}/Overview`);

    tR += `---
type: mission
mission_name: ${JSON.stringify(name)}
status: planning
tags:
  - mission
---

# ${name}

## Mission brief
- **Hook:**
- **Objective:**
- **Stakes:**
- **Opening scene:**
- **Resolution:**

## Key elements
- **Locations:**
- **Characters:**
- **Anomalies:**

## Golden path

The intended route through the mission. Add or remove steps and branches as needed.

\`\`\`mermaid
flowchart TD
    Start["Briefing / hook"] --> Lead["First lead"]
    Lead --> Investigate["Investigate"]
    Investigate --> TurningPoint["Turning point / reveal"]
    Investigate -. "complication" .-> TurningPoint
    TurningPoint --> Choice{"Final choice"}
    Choice --> Resolution["Resolution"]
\`\`\`

## GM notes
- **Secrets:**
- **If the agents go off path:**
`;
  }
}
%>
