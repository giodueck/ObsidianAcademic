# Open Systems Interconnection
Conceptual model that standardizes the way a [[Computer network]] handles communications. It presents 7 layers of communication and can help visualize and simplify networks.

## Layers
#### Host layers
| Data     | Layers          | Description |
| -------- | --------------- | ----------- |
| Data     | 7. Application  | Network process to application |
| Data     | 6. Presentation | Data representation & encryption |
| Data     | 5. Session      | Inter-Host communication |
| Segments | 4. Transport    | End-to-End connections and reliability |
#### Media layers
| Data     | Layers          | Description |
| -------- | --------------- | ----------- |
| Packets  | 3. Network      | Path determination & IP |
| Frames   | 2. Data link    | [[MAC]] & LLC (physical addressing) |
| Bits     | 1. Physical     | Media, signal & binary transmission |