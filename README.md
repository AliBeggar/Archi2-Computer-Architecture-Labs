# Computer Architecture 2 (`ARCH2`) - Logisim Circuits & Labs

A structured collection of digital logic circuits, tutorial implementations, and hardware simulations built in **Logisim** for the **Computer Architecture 2 (`ARCH2`)** module at the **École Nationale Supérieure d'Informatique (ESI)**.

---

## About the `ARCH2` Course

**Computer Architecture 2** (*Architecture des Ordinateurs 2* — 4 Credits, Coefficient 4, 30h Lectures / 30h Tutorials) builds on `ARCH1` with the goal of designing an elementary computer from the ground up. It focuses on understanding each datapath component, mastering information flow through memory and control circuits, and designing communication mechanisms between the CPU and peripherals.

### Syllabus Overview

| Chapter | Topic | Key Concepts Covered |
| :---: | :--- | :--- |
| **I** | **Memories (15h)** | Semiconductor memory technology, ROM/PROM/EPROM/EEPROM, SRAM & DRAM, Sequential memories (FIFO / LIFO), Associative memories (CAM), and Cache memory. |
| **II** | **I/O Devices & Controllers (3h)** | Peripheral types, controller architecture, CPU/peripheral dialogue interfaces, and controller commands. |
| **III** | **I/O Transfer Modes (3h)** | Programmed I/O, status polling, interrupt-driven I/O, Direct Memory Access (DMA), and I/O channels (selector & multiplexer). |
| **IV** | **Interrupt Systems (3h)** | Internal, I/O, and hardware interrupts; detection, context save/restore, acknowledgment, masking, hierarchical levels, and vectored interrupts. |
| **V** | **The Sequencer (3h)** | Control unit operation, hardwired sequencers, and microprogrammed sequencers. |

---

## Featured Module: Tutorial No. 2 — Read-Only Memories (ROM)

All 8 exercises from the **Read-Only Memories** tutorial are implemented in Logisim using **custom bipolar transistor matrices** rather than predefined ROM components.

| # | Circuit | Description & Key Specs |
| :---: | :--- | :--- |
| **01** | **Elevator Control System** | 4-floor (0–3) controller taking current position (`E1, E0`) and called floor (`A1, A0`) to output direction (`UP`, `DOWN`, `STOP`) and 2-bit travel distance (`D1, D0`) via a single transistor-based ROM. |
| **02** | **Priority Arbiter** | Resolves shared central memory conflicts across 3 processors (`P2 > P1 > P0`), granting an authorization signal to the highest-priority requester. |
| **03** | **Prime Number Generator** | Analyzes a 4-bit integer (`0–15`) to output primality (`PRIME`), the next prime number (`NEXT3..NEXT0`, returning `13` for `N = 13`), and its 3-bit divisor count (`DIV2..DIV0`). |
| **04** | **2-Bit Multiplication Circuit** | Multiplies two 2-bit numbers (`A1A0 × B1B0`) using a minimal network of **2-input** transistor-based ROMs. |
| **05** | **7-Segment Decoder + Error Detection** | Decodes 4-bit inputs (`D3..D0`) to active-high display segments (`a–g`) for digits `0–9` and raises an `ERR` flag for invalid codes (`10–15`). |
| **06** | **Traffic Light Controller** | 8-state North-South / East-West intersection controller with safety clearance phases (`NS/EW` Red, Yellow, Green + `NEXT1, NEXT0`) built with a 16-word ROM. |
| **07** | **4-Bit Calculation Unit (ALU)** | 4-bit ALU composed of 4 modular slices (`M0–M3`) performing `A+B`, `A OR B`, `A AND B`, and `NOT A` using ROMs and high-impedance logic, generating `Zero`, `Overflow`, `Carry`, and 8-bit program addresses (`ADR0–ADR3`). |
| **08** | **Washing Machine Timer** | 16-cycle synchronous phase controller stepping through Washing (5 cycles), Rinsing (4 cycles), Spin (4 cycles), and Shutdown (3 cycles) using a 16-word ROM. |
