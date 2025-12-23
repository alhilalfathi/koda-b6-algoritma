```mermaid
flowchart TD
    A@{ shape: circle, label: "Mulai" }
    B@{ shape: lean-r, label: "Input: Angka"}
    d@{ label: "Angka : 2"}
    C@{ shape: diamond, label: "Angka % 2 == 0"}
    F@{ shape: lean-r, label: "Output: Angka Bilangan Genap"}
    G@{ shape: lean-r, label: "Output: Angka Bilangan Ganjil"}
    H@{ shape: dbl-circ, label: "Selesai"}

A --> B --> C -- True --> F
C -- False --> G
F & G --> H
```