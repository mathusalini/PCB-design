# Transformerless Power Supply (TPS)

## What is a Transformerless Power Supply?
A **Transformerless Power Supply** is a type of power supply circuit that converts **AC mains voltage (230 V / 110 V)** into a **low-voltage DC output** **without using a transformer**.  
Instead of voltage transformation, it uses a **capacitive current-limiting method** to safely supply a small amount of current to low-power electronic circuits.

> ⚠️ **Note:** Transformerless power supplies do **not provide electrical isolation** from the mains supply and must be used only in **fully enclosed, low-power applications**.

---

## Basic Concept of Transformerless Power Supply
The core idea behind a transformerless power supply is **current limitation rather than voltage reduction**.

- A **non-polarized capacitor** connected in series with the AC input limits the current.
- This limited current is converted from AC to DC using a **bridge rectifier**.
- A **filter capacitor** smooths the DC voltage.
- A **zener diode or voltage regulator** maintains a fixed output voltage.

---

## Working Principle
1. **AC mains supply** is applied to the circuit.
2. A **series capacitor** restricts the amount of current flowing into the circuit.
3. A **bridge rectifier** converts AC to pulsating DC.
4. A **filter capacitor** reduces ripple and smooths the output.
5. A **zener diode/regulator** clamps the voltage to a safe DC level.
6. The circuit provides **low-current DC output** for small electronic loads.

---

## Where is Transformerless Power Supply Used?

### Applications
Transformerless power supplies are commonly used in:
- LED bulbs and LED drivers  
- Night lamps  
- Smart switches and touch panels  
- Power indicator circuits  
- Small IoT devices (fully enclosed)  
- Low-power control circuits  

### Not Suitable For
- Audio amplifiers  
- Mobile chargers  
- Laboratory power supplies  
- Devices with exposed metal parts  
- High-current applications  

---

## Advantages
- Compact and lightweight  
- Low cost  
- Simple circuit design  
- No bulky transformer required  

---

## Disadvantages
- No electrical isolation (shock hazard)  
- Limited current capability  
- Unsafe for open or user-accessible circuits  
- Not suitable for high-power devices  

---

## Why This Circuit is Studied
- Demonstrates real-world industrial power supply design  
- Helps understand **mains-level PCB safety**  
- Useful for learning schematic design and PCB layout in KiCad  
- Commonly used as a **theoretical and design practice project**

---

## Brief Concept
A transformerless power supply converts AC mains voltage into low-voltage DC using a capacitive current-limiting method without employing a transformer, suitable only for low-power enclosed applications.


# KiCad Project – Footprint Assignment Procedure

## Step 1: Create a New Project
- Open **KiCad**
- Click **File → New Project**
- Enter the project name and choose the save location
- KiCad will create:
  - Schematic file (`.kicad_sch`)
  - PCB file (`.kicad_pcb`)

---

## Step 2: Open the Schematic Editor
- Double-click the **schematic file**
- The **Schematic Editor** window opens
- This is where the circuit diagram is created

---

## Step 3: Select and Place Components
- Click **Place Symbol**
- Select and place all required components in the schematic



### Components Used
- **Diodes**
  - 4 × `1N4007` (Bridge rectifier)
- **Capacitors**
  - Polarized capacitors (electrolytic)
  - Non-polarized capacitors
- **Zener diodes**
- **Resistors**
- **LED**
- **Screw terminals**
- **Voltage regulator**
  - `LM7805`
- **Connect wires and annotate the schematic**

---

## Step 4: Assign Footprints
- After completing the schematic:
  - Click **Tools → Assign Footprints**
- The **Symbol : Footprint Assignments** window opens

### Footprint Assignment Details
- **1N4007 diodes**
  - `Diode_THT:D_DO-41_SOD81_P10.16mm_Horizontal`
- **Polarized capacitors**
  - `Capacitor_THT:CP_Radial`
- **Non-polarized capacitors**
  - `Capacitor_THT:C_Disc` or `C_Rect`
- **Resistors**
  - `Resistor_THT:R_Axial_DIN0207`
- **LED**
  - `LED_THT:LED_D5.0mm`
- **Screw terminals**
  - `TerminalBlock:TerminalBlock_1x02`
- **LM7805 voltage regulator**
  - `Package_TO_SOT_THT:TO-220-3_Vertical`

- Assign the appropriate footprint to **each symbol**
- Click **OK** to save footprint assignments

---

## Result
- All schematic symbols are now linked to physical PCB footprints
- The design is ready for:
  - PCB layout
  - Component placement
  - Routing tracks

---

## Conclusion
Footprint assignment is a critical step in KiCad that connects the schematic design to real-world PCB components. Correct footprint selection ensures proper component placement, soldering, and manufacturing accuracy.
