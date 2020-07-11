# Parametered projections for Coriolis

This package provides useful projections and tools to build projections that can be customized.

# Install

```sh
npm install --save @coriolis/parametered-projection
```

# Usage

```javascript
import { lastPayloadOfType } from '@coriolis/parametered-projection'

// This projection would return an array of all payloads of events with type "target event type"
const myProjection = ({ useState, useProjection }) => (
  useState(0),
  useProjection(lastPayloadOfType('target event type')),
  (list, event) => [...list, event]
)
```

Of course this code sample is not doing anything interesting. But parametered projections are really helpful in real world.
