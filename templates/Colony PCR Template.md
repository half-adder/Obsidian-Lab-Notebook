Following [NEB's protocol](https://www.neb.com/protocols/0001/01/01/taq-dna-polymerase-with-standard-taq-buffer-m0273).

| Component                        | 25 μl reaction | x{{VALUE}} (uL) |
| -------------------------------- | -------------- | ------- |
| 10X Standard Taq Reaction Buffer | 2.5 μl         |   |
| 10 mM dNTPs                      | 0.5 µl         |     |
| 10 µM Forward Primer             | 0.5 µl         |    |
| 10 µM Reverse Primer             | 0.5 µl         |    |
| Template DNA                     | variable       |   |
| Taq DNA Polymerase               | 0.125 µl       |     |
| Nuclease-free water              | to 25 µl       |    |
<!-- TBLFM: $3=($2 * ({{VALUE}} * 1.2));%.2f -->

Cycling conditions:

| Step                 | Temp | Time          |
| -------------------- | ---- | ------------- |
| Initial Denaturation | 95°C | 30 seconds    |
| 30 cycles            | 95°C | 15-30 seconds |
|                      | Tm   | 15-60 seconds |
| Final Extension      | 68°C | 5 minutes     |
| Hold                 | 12C  |               |