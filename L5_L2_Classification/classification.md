# L5 Narrow / L2 General Classification — K_ROBOTWIN
**Platform:** Anticloud | **Tier:** TIER_5_WORLD_NEURO_EMBODIED | **PAX:** 27B
**IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg | **License:** Apache-2.0

## L5 Narrow
K_ROBOTWIN implements learning from demonstration (LfD) using a digital twin: demonstrations are recorded in physical space, validated in K_HELIX physics simulation, then used to train robot policies. Narrow scope: TIER_9 robot manipulation and navigation tasks.

## L2 General
L2 General: K_ROBOTWIN's LfD capabilities apply to all TIER_9 robot platforms. The same twin-based learning works for arm manipulators (L_MOVEIT2) and mobile robots (L_ROS2NAV).

## PAX 27B Integration
PAX 27B analyzes recorded demonstrations and generates structured task descriptions that guide the policy learning process, improving sample efficiency.

## AIOSS Audit Chain
Every demonstration (recording hash + physics validation result + learned policy hash + success rate on validation) is chained: H_n = SHA3-256(H_{n-1} || entry_hash_n || timestamp_n).
Offline-verifiable, tamper-evident, zero cloud dependency.

## Regulatory / Compliance
ISO 13482 (robot safety). IEC 61508 (safety-critical learning).
