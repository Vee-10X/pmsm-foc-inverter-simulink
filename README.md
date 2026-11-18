# pmsm-foc-inverter-simulink
Simulink model of a pmsm drive with a three-phase inverter, PWM and field-oriented control

# Modelling and Simulation of Field-Oriented Control of a Permanent Magnet Synchronous Motor with a Three-Phase Inverter in MATLAB/Simulink

Status: In progress (started 18 November 2026)

## Overview
This project models a permanent magnet synchronous motor (PMSM) drive in MATLAB/Simulink. The model includes a DC source, a three-phase inverter with PWM switching, the PMSM and its sensors, and is controlled with field-oriented control (FOC). The drive is evaluated on speed tracking and load-disturbance rejection. A simpler dq-frame model is used to design the controller gains and to cross-check the full model.

## Aim
To model a PMSM drive supplied through a three-phase inverter and control it with field-oriented control, so that its speed tracking and load-disturbance rejection can be evaluated.

## Objectives
- Model the power stage: a DC source, a three-phase two-level inverter and a PMSM in Simulink/Simscape Electrical.
- Implement PWM switching for the inverter and verify the gate signals and phase voltages.
- Add sensing: phase currents, rotor speed and rotor angle, with Clarke and Park transformations to obtain id and iq.
- Implement field-oriented control with decoupling, d- and q-axis PI current loops (id* = 0) and an outer PI speed loop.
- Evaluate speed-reference tracking (rise time, overshoot, settling time) and load-disturbance rejection (speed dip and recovery time).
- Cross-check the results against a simple dq-frame reference model and a published simulation, and explain the differences.
- Document assumptions, limitations and results, with all figures reproducible from the repository.

## Scope and limitations
- Included: switching inverter, PWM, PMSM, current and speed sensors, FOC with three PI loops.
- Assumed: constant DC supply (no battery model), ideal sensors, linear motor magnetics, no thermal effects.
- Not claimed: efficiency, losses, temperature or a full vehicle model.

## Repository structure
- `scripts/`: parameters and the dq-frame reference simulation (`foc_reference.m`)
- `model/`: Simulink/Simscape model files (to be added)
- `results/`: figures and tables
- `docs/`: project brief and notes

## Results
To be completed. Only results produced by the model will be shown here.

## References
- Motor parameters and the reference dq-frame simulation follow: Tripathi, H., Marahatta, K., Gupta, B. K., Yadav, N. K., Shrestha, S. (2023). Modelling and Simulation of Field-Oriented Control of Permanent Magnet Synchronous Motor. Journal of Engineering and Sciences, 2(1), 88-92.
