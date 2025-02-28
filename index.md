## FSM 1: No Branching

```mermaid
stateDiagram
    [*] --> S0
    S0 --> S1 : a
    S1 --> [*]
```

This is the first finite state machine showing a transition from start to state S0, then to S1 on input 'a', and finally ending.

## FSM 2: Branching States

```mermaid
stateDiagram
    [*] --> S0
    S0 --> S1 : x
    S0 --> S2 : y
    S1 --> [*]
    S2 --> [*]
```

This is the final text.