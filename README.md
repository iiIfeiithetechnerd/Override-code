# VEX V5 Override code
This is a lightweight, concurrent safety background process.

## Tech stack and concepts
* **Language:** C++ (VEXcode V5 Pro Framework)
* **Concurrency:** `vex::thread` for parallel background processing
* **Telemetry Data:** Real-time extraction from motors, gathering temperature (Celcius), velocity (RPM), and current draw (Amperes)

## How to clone
1. Clone this repository directly onto your local VEX workspace:

   ```
   clone https://github.com/iiIfeiithetechnerd/Override-code.git
   ```
   
3. Open the project folder in **VEXcode V5** or **VS Code with the VEX Extension**.
4. Map all high-stress motors inside the `monitored_motors` array
5. Initialize the daemon at the beginning of `main()` via:

   ```
   vex::thread safety_thread = vex::thread(motor_safety_daemon);
   ```

