# Syllabus Mapping: Workshop Demo Cells to Weekly Goals

---

## Cell 1 -- Imports

Syllabus connection:
- Week 2: Python and conda setup. Install Brian2 via conda, set up environment.
- Week 5: Open science workflow. The environment.yml pins all dependency versions.

---

## Cell 2 -- Neuron Equations (Gunay et al. 2015 kinetics)

Syllabus connection:
- Week 3: Brian2 basics. Differential equations, NeuronGroup, how simulators step through time.
- Week 4: Reading the paper. Parameters come from Table 1, channel kinetics from Gunay et al. (2015). These are Boltzmann steady-state formulations, not classic HH alpha/beta.

---

## Cell 3 -- Neuron Groups (GF, TTMn, PSI, DLMn)

Syllabus connection:
- Week 3: Brian2 basics. NeuronGroup is the basic building block. Initial conditions from steady-state at resting potential.
- Week 4: Paper reading. Figure 2A shows the four-cell architecture: GF, TTMn, PSI, DLMn. Each cell has a defined role in the escape pathway.
- Week 6: Building the model. The single-compartment version here is the starting skeleton. The paper uses multi-compartment neurons (1-3 sections, 51 segments each).

---

## Cell 4 -- Synapses (gap junctions + chemical synapse)

Syllabus connection:
- Week 4: Paper reading. The paper emphasizes that gap junction conductance reduction with age accounts for increased escape latency. g_gap young = 135 uS, old = 34.5 uS.
- Week 6: Building the model. Three connections: two gap junctions (GF->TTMn, GF->PSI) and one chemical synapse (PSI->DLMn with double-exponential kinetics).

---

## Cell 5 -- Stimulus and Simulation

Syllabus connection:
- Week 3: Brian2 simulation mechanics. Network construction, network_operation for stimulus injection, run() method.
- Week 6: First simulation run. Apply stimulus to GF and propagate through the circuit.

---

## Cell 6 -- Latency Measurement

Syllabus connection:
- Week 4: Paper reading. The paper measures latency as time from stimulus to AP peak, plus 0.35 ms NMJ delay. Experimental values: young TTM = 0.93 ms, DLM = 1.44 ms; old TTM = 1.22 ms, DLM = 1.85 ms.
- Week 7 (future): Refine latency measurement. Compare model output to paper values and debug discrepancies.

---

## Cell 7 -- Voltage Traces

Syllabus connection:
- Week 2: Basic plotting with matplotlib.
- Week 6: Validate model behavior visually. Signal propagation order: GF -> TTMn/PSI -> DLMn.

---

## Cells 8-9 -- Parameter Sweep and Latency Plot

Syllabus connection:
- Week 6: Parameter exploration. Sweep g_gap and observe the latency trend.
- Week 8 (future): Reproduce Figure 2C quantitatively. Explore additional parameters (Na/K conductances, Figure 3; anatomic changes, Figure 4).
- Week 9 (future): Compare sweep output to the published latency curves.

---

## Cell 10 -- Summary

Maps all cells to syllabus weeks 1-6 and lists remaining work for weeks 7-11.
