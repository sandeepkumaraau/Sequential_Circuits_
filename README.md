# Design of Digital Circuits - Project 2: Sequential Circuits

This repository contains the solution for the second project of the Design of Digital Circuits (DDC) course (Summer 2024). The project focuses on the design, implementation, and testing of various sequential circuits using the Logisim educational tool.

## Team Members
* Michiliia Gureva
* Sandeep Kumar
* Stephen Nnamani
* Vulcu Horia - Rares
* Yew Heng Ngoh

## Project Overview
The core of this project is to build fundamental sequential logic components from the ground up and then use them to create more complex circuits.The exercises progress from implementing basic flip-flops to constructing a sequence detector, a shift register, and finally, a serial adder that utilizes the previously built components.

**Deliverables:**
* [cite_start]Logisim simulation file (`.circ`) 
* [cite_start]Presentation slides (`.pdf`) showing the solutions 

## Implemented Circuits

The project is divided into five main parts, each building upon the last.

### 1. Positively-Triggered D-Flip-Flop
* **Description:** A D-Flip-Flop that loads the input signal `d` on the rising edge of the clock cycle.
* **Features:** Includes a synchronous `Reset` input in addition to the data and clock inputs.
* **Implementation:** The solution includes the Logisim circuit  and a chronogram to demonstrate its correct functionality.

### 2. Negatively-Triggered JK-Flip-Flop
* **Description:** A JK-Flip-Flop that performs its state transition on the falling edge of the clock signal. It provides a defined behavior for the J=1, K=1 input combination, unlike a standard RS-Flip-Flop.
* **Features:** Equipped with an asynchronous `Reset` input.
* **Implementation:** The circuit was designed and tested in Logisim. A chronogram is provided to verify its behavior.

### 3. Sequence Detector
* **Description:** A circuit that detects two specific binary patterns from a two-bit input stream (X0, X1) and outputs Z=1 when a sequence is found.
* **Target Sequences:**
    * Sequence 1: `00; 01; 11` 
    * Sequence 2: `00; 11` 
* **Implementation:** The design process included creating a finite state machine , deriving a transition table , finding minimal Boolean equations , and implementing the final circuit in Logisim using the D-Flip-Flops created in the first exercise.

### 4. Shift Register
* **Description:** A 4-bit unidirectional shift register that supports right-shifting. The register is capable of parallel input and parallel output.
* **Features:**
    * **Shift:** Shifts the register content to the right.
    * **Load:** Loads parallel data into the register.
    * **Store:** Holds the current value if both Shift and Load are inactive.
    * **Reset:** An asynchronous Reset for all flip-flops.
* **Implementation:** A 1-bit shift register module was first created , which was then used to build the 4-bit version. This circuit exclusively uses the custom-made D-Flip-Flops.

### 5. Serial Adder
* **Description:** A circuit that adds two 4-bit binary numbers serially.It uses two shift registers , one full adder, and a D-Flip-Flop to store the carry bit between additions.
* **Operation:**
    1.  An initial number is loaded into Register B.
    2.  As the clock cycles, the contents of both registers are shifted right, one bit at a time, into a full adder.
    3.  The sum bit from the full adder is shifted into the serial input of Register A.
    4.  The carry-out bit is stored in a separate D-Flip-Flop for the next clock cycle's addition.
    5.  The final accumulated sum is stored in Register A.
* **Implementation:** The complete 4-bit serial adder was constructed in Logisim , using the 4-bit shift registers from the previous task.

## How to Use
To view and test the circuits, open the `.circ` file with [Logisim](http://www.cburch.com/logisim/). The main canvas of each file contains the final implementation for each exercise.

## Acknowledgments
* **Course:** Design of Digital Circuits (DDC) - Summer 2024 
* **Instructor:** Markus Gutmann
