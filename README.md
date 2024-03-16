# Matlab System Model

Mathematical model of the ASTRAEUS-01 spacecraft and its subsystems.

## Interface Control Document

### ADCS

| mode | quantity | mathematical variable name | model variable name | justification |
| -- | -- | -- | -- | -- |
| _input_ | moment of inertia | $...$ | `...` | required for attitude control calculations |
| _output_ | attitude | $...$ | `...` | used in effective area calculations |
| _output_ | position | $...$ | `...` | used in effective area calculations |

### EPS

| mode | quantity | mathematical variable name | model variable name | justification |
| -- | -- | -- | -- | -- |
| _input_ | temperature | $...$ | `...` | required for battery performance calculations |
| _input_ | attitude | $...$ | `...` | required for effective area calculations |
| _input_ | position | $...$ | `...` | required for effective area calculations |
| _output_ | heat dissipated by power electronics | $Q_{EPS}$ | `...` | used in thermal balancing calculations |
| _output_ | electrical power delivered to payload camera module | $P_{PC}$ | `...` | used in computational load calculations |
| _output_ | electrical power delivered to payload data handling module | $P_{PDH}$ | `...` | used in computational load calculations |
| _output_ | electrical power delivered to communications module | $P_{comms}$ | `...` | used in computational load calculations |

### Other Computational Electronics

#### Payload Camera

| mode | quantity | mathematical variable name | model variable name | justification |
| -- | -- | -- | -- | -- |
| _input_ | electrical power delivered | $P_{PC}$ | `...` | required for computational load calculations |
| _output_ | heat dissipated by payload camera module | $Q_{PC}$ | `...` | used in thermal balancing calculations |

#### Payload Data Handler

| mode | quantity | mathematical variable name | model variable name | justification |
| -- | -- | -- | -- | -- |
| _input_ | electrical power delivered | $P_{PDH}$ | `...` | required for computational load calculations |
| _output_ | heat dissipated by payload data handling module | $Q_{PDH}$ | `...` | used in thermal balancing calculations |

#### Communications Module

| mode | quantity | mathematical variable name | model variable name | justification |
| -- | -- | -- | -- | -- |
| _input_ | electrical power delivered | $P_{comms}$ | `...` | required for computational load calculations |
| _output_ | heat dissipated by communications module | $Q_{comms}$ | `...` | used in thermal balancing calculations |

### Structures

| mode | quantity | mathematical variable name | model variable name | justification |
| -- | -- | -- | -- | -- |
| _input_ | uniform temperature | $T$ | `...` | required for thermal cycling calculations |
| _output_ | moment of inertia | $...$ | `...` | used in attitude control calculations |

### Thermal

| mode | quantity | mathematical variable name | model variable name | justification |
| -- | -- | -- | -- | -- |
| _input_ | attitude | $...$ | `...` | used in effective area calculations |
| _input_ | position | $...$ | `...` | used in effective area calculations & Earth's shadow check |
| _input_ | heat dissipated by power electronics | $Q_{EPS}$ | `...` | required for thermal balancing calculations |
| _input_ | heat dissipated by payload camera module | $Q_{PC}$ | `...` | required for thermal balancing calculations |
| _input_ | heat dissipated by payload data handling module | $Q_{PDH}$ | `...` | required for thermal balancing calculations |
| _input_ | heat dissipated by communications module | $Q_{comms}$ | `...` | required for thermal balancing calculations |
| _output_ | uniform temperature | $T$ | `...` | used in battery performance and thermal cycling calculations |

