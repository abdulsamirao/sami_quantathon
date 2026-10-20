# ECHO — Case Report
**Entangled Minds: The Quantathon · Qubits Qrew, NED University**
Notebook: `ECHO_Quantathon_Solution.ipynb` (Modules 01–06 all solved; stretch modules 02, 04 and 06 all attempted)

---

## 1. Final Theory / Verdict

**ECHO never sent a message faster than light. Zara mistook an echo for a voice.** Her detectors agreed, and agreement is exactly what a pre-agreed shared secret also produces. Even genuine entanglement carries no usable information on its own.

I also conclude that **the experiment's trigger was not a chance event.** The "random" quantum seed was tuned to a 30/70 split, which looks designed, so someone chose it.

| Claim | Confidence | Basis |
| No faster-than-light message was sent | **Very high (100%)** | Established theorems (no-signalling) and experiments I ran (M03, M06) |
| Zara's "proof of linkage" proved nothing by itself | **Very high** | A classical shared secret reproduces her observation (M03) |
| The seed was biased and its bias looks deliberate | **Very high** | Exact P(1) = 0.300; the angle matches 2·arcsin√0.30 (M02) |
| Who configured it | **Low** | Physics cannot identify a person; see §5 |

My working suspicion on the human mystery is **Sana Rao**, because she alone had full access to the records and could rewrite what logs say or when they say it. The evidence does not exclude **Prof. Vance**, who had the knowledge to plant or expose a flaw. We can not claim certainty. Nothing in the modules can name a person.

the machine name:
run time revealed by Module 0:
the note beneath her message from Module 05: 

---

## 2. Evidence and Clues (the three that matter most)

1. **Agreement is not entanglement (M03).** A secret coin flip agreed beforehand gives the same 00/11 histogram as the Bell pair. Only a CHSH test separates them: quantum S ≈ 2.83, classical limit 2.
2. **The seed was tuned, not random (M02).** The recovered circuit `ry(1.159)` gives P(1) = sin²(0.5795) = **0.2999**. The angle equals 2·arcsin(√0.30) = 1.1593. A random slip would not land on a round 30%.
3. **The message could only arrive with classical help (M06).** The recovered teleportation circuit delivers the state ≈100% of the time with the two classical bits and ≈50% without. Without the bits, Bob's qubit is maximally mixed for every possible message.

Supporting: the damaged message decodes to **ECHO** (M05). ARIA's "it changed when observed" excuse fits real physics only for a random scramble from a mid-way measurement, not a chosen edit (M04).

---

## 3. Evidence Board

| Type | Item |
|---|---|
| **FACT** | M01: X gives 1 every shot; H gives ≈50/50; H,H gives 0 every shot; X on qubits 0 and 2 gives `101` |
| **FACT** | M02: Exact P(1) of the recovered seed is 0.2999 (≈30% ones, ≈70% zeros over many shots), far outside a 50/50 coin |
| **FACT** | M03: Bell pair gives only 00 and 11. A classical shared secret gives the same Z-basis result. CHSH on the Bell pair gives S ≈ 2.83 (>2). Bob's P(1) ≈ 0.5 whatever Alice does |
| **FACT** | M04: H,H gives 0; H,measure,H gives 50/50; X,H,H gives 1; H,X,H gives 0 |
| **FACT** | M05: Majority vote decodes the 96-bit stream to "ECHO". 20 of 32 triples had one flipped bit. Two flips in a triple decode wrongly and silently |
| **FACT** | M06: Recovered teleportation circuit: ≈100% with the two bits, ≈50% without. Bob's state without bits equals I/2 for 8 random states |
| **CLAIM** | Zara: ECHO sent a message faster than light |
| **CLAIM** | Vance: "ECHO was never real" |
| **CLAIM** | Sana: "I only deleted a corrupted log" |
| **CLAIM** | Bilal: "I warned her" (his report is now missing) |
| **CLAIM** | ARIA: "No unauthorised command was issued" |
| **INFERENCE** | Her detectors' agreement was never tested against the shared-secret explanation, so it proves no link |
| **INFERENCE** | The 30/70 seed was deliberately set: the angle matches a round probability |
| **INFERENCE** | ARIA's excuse cannot explain a log edited to a chosen value, since the observer effect gives a random result and ordinary logs are classical data |
| **INFERENCE** | ECHO moved a quantum state at best; the information needed to read it travels classically, at or below light speed |
| **OPEN QUESTION** | Who configured the seed and schedule: Sana, Vance, someone else, or an innocent miscalibration? |
| **OPEN QUESTION** | Was Sana's deleted log scrambled or rewritten? Where is Bilal's missing report? |
| **OPEN QUESTION** | Did Zara ever run a Bell test, or record the two classical bits? |

---

## 4. Experiments and Results

All experiments ran on Qiskit's ideal `AerSimulator`. Circuits, histograms and predictions are in the notebook.

| Module | Experiment | Prediction | Result |
| 01 | X; H; H,H; X on q0 and q2 | 1; 50/50; 0; `101` | As predicted |
| 02 | Recovered seed `ry(1.159)`; exact statevector plus 20,000 shots; fair-coin test | Biased if sin²(θ/2) ≠ 0.5 | P(1) = 0.300; 95% CI excludes 0.5; chi-square p ≈ 0. About 76 shots would detect a bias this large at 95% power |
| 03 | Bell pair; classical shared secret; Z/X basis change; CHSH; no-signalling | Agreement in both; S = 2√2 quantum, ≤2 classical; Bob's marginal fixed | S ≈ 2.83; the secret cannot exceed 2 (all 16 deterministic strategies checked); Bob's marginal ≈ 0.50 for every Alice action |
| 04 | H,H vs H,measure,H; XHH; HXH; random sequences vs hand-built predictor | 0; 50/50; 1; 0 | As predicted. The predictor matched Qiskit on every random sequence |
| 05 | Majority vote; failure demo; no-cloning; 3-qubit bit-flip code | Decodes with ≤1 flip per triple; fails at 2 | "ECHO". 1 flip corrected, 2 flips fail. CNOT "copy" of \|+⟩ has fidelity 0.25 with \|+++⟩ |
| 06 | Recovered teleportation circuit; no-correction run; density-matrix check for 8 random states | ≈100% with bits; ≈50% without; Bob's state = I/2 | As predicted |

---

## 5. Interpretation

**The crux is whether the detectors could send a message or only agree.** They only agreed.
- Agreement is reproduced by any pre-agreed secret (M03 Silver).
- CHSH shows the quantum pair is genuinely entangled (S > 2), but no secret could have produced that. This is not the same as a communication channel.
- Bob's statistics never depend on what Alice does (no-signalling), so no message can ride on the correlation.
- In teleportation, the state arrives only with two ordinary classical bits (M06), so the part that "travels" is a state, while the key for reading it travels classically.

**On the human mystery:** the seed's designed 30/70 bias means the run was not left to chance. That fits someone with configuration or records access (Sana's role, or ARIA's operator), but also a sincere error by Zara. ARIA's observer-effect defence does not hold for a log edited to a chosen value. I treat this as a pointer, not proof.

---

## 6. Alternative Explanation

**The strongest rival: no sabotage at all.** Zara sincerely over-interpreted real entanglement. The 1.159 angle was an honest calibration choice (she wanted a 30% trigger on purpose), and the log was corrupted by accident.

I prefer my theory because (a) the over-interpretation is common to both theories, and (b) the rival must explain why a deleted log and a missing report coincide with the run. I would drop my suspicion of a person if the configuration history shows Zara herself set the angle.

---

## 7. Next Experiment

1. **Configuration audit:** check the commit/edit history and timestamps of ARIA's schedule and seed settings against Sana's deleted log.
   - If Zara set 1.159 herself, the innocent theory wins.
   - If someone else changed it near the run, the sabotage theory gains support.
2. **Hardware Bell test:** run CHSH on ECHO's real detectors with randomly chosen settings and spacelike separation.
   - Expect S ≈ 2.8 (minus noise) with Bob's marginals fixed at 50/50 under my theory.
   - Bob's marginals shifting with Alice's setting would mean she really signalled (quantum mechanics forbids this).
   - S ≤ 2 would mean the "entanglement" was a shared secret.

---

## 8. Limitations

- Everything ran on an **ideal simulator**: no noise, no detector loopholes. A simulation shows what quantum mechanics predicts and is not itself a Bell test.
- The experiments **cannot identify a person**. The Sana suspicion rests on her access and role, not on a measurement.
- The seed's bias being deliberate is an **inference**. A designed 30% and a coincidence are not statistically separable from one circuit alone.
- I do not know what ECHO's real hardware did.
