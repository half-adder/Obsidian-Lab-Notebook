Following [NEB's Q5 PCR Protocol](https://www.neb.com/protocols/2013/12/13/pcr-using-q5-high-fidelity-dna-polymerase-m0491). Primers: 

| Component        | 25 uL Rxn | x{{VALUE}}.2 (uL) |
| ---------------- | --------- | ----------------- |
| 5X Q5 Rxn Buffer | 5 uL      |                   |
| 10 mM dNTPs      | 0.5 uL    |                   |
| 10 uM Fwd Primer | 1.25 uL   |                   |
| 1 uM Rev Primer  | 1.25 uL   |                   |
| Template DNA     | variable  |                   |
| Q5 Polymerase    | 0.25 uL   |                   |
| H2O              | to 25     |                   |

<!-- TBLFM: $3=($2 * ({{VALUE}} * 1.2));%.2f -->

| Step                 | Temp | Time               |
| -------------------- | ---- | ------------------ |
| Initial Denaturation | 98C  | 30 seconds         |
| 35 cycles            | 98C  | 5-10 seconds       |
|                      | Ta   | 10-30 seconds      |
|                      | 72 C | 20-30 seconds / kb |
| Final Extension      | 72C  | 2 minutes          |
| Hold                 | 12C  |                    |
