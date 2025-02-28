```mermaid
    info
```


## FSM 1: No Branching

<div class="mermaid">
stateDiagram
    direction LR
    classDef accepting font-weight:bold, stroke-width:3px

    S0 --> S1 : a

    class S1 accepting
</div>

This is the first finite state machine showing a transition from start to state S0, then to S1 on input 'a', and finally ending.

## FSM 2: Branching States

<div class="mermaid">
stateDiagram
    direction LR

    [*] --> S0
    S0 --> S1 : x
    S0 --> S2 : y
    S1 --> [*]
    S2 --> [*]
</div>

## With styling

<div class="mermaid">
   stateDiagram
   direction TB

   accTitle: This is the accessible title
   accDescr: This is an accessible description

   classDef notMoving fill:white
   classDef movement font-style:italic
   classDef badBadEvent fill:#f00,color:white,font-weight:bold,stroke-width:2px,stroke:yellow

   [*]--> Still
   Still --> [*]
   Still --> Moving
   Moving --> Still
   Moving --> Crash
   Crash --> [*]

   class Still notMoving
   class Moving, Crash movement
   class Crash badBadEvent
   class end badBadEvent
</div>

<script type="module">
    import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.esm.min.mjs';
    mermaid.initialize({ startOnLoad: true });
</script>