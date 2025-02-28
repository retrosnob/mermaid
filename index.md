<script type="module">
    import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.esm.min.mjs';
    mermaid.initialize({ startOnLoad: true });
</script>

## FSM 1: No Branching

<div class="mermaid">
stateDiagram
    direction LR
    classDef accepting font-weight:bold, stroke-width:3px

    S0 --> S1 : a

    class S1 accepting
</div>

This is the first finite state machine showing a transition from start to state S0, then to S1 on input 'a', and finally ending.

## Binary Search Tree

<div class="mermaid">
graph TD
    A[50] 
    A --> B[30]
    A --> C[70]
    B --> D[20]
    B --> E[40]
    C --> F[60]
    C --> G[80]

    %% Define the global style
    classDef allNodes fill:#ffffff,stroke:#000000,stroke-width:2px;

    %% Apply the style to all nodes
    class * allNodes;    
</div>

## Flowchart

<div class="mermaid">
flowchart TD
    Start([START]) 
    Input[/Input int n/]
    InitR[ r = 0 ]
    Decision{ n > 0 }
    CalcR["r = (r * 10) + (n mod 10)"]
    UpdateN[ n = n / 10 ]
    Output[/ output r /]
    Stop([STOP])

    %% Flow
    Start --> Input --> InitR --> Decision
    Decision -->|yes| CalcR --> UpdateN --> 
    Decision -->|no| Output --> Stop
    
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


```
import math

def thisiscode(param1):
    return math.log(param1, 2)

```






