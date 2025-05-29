# Calibration and Testing for DIY Magneto Bench Tester

This guide outlines the procedures for calibrating and testing the DIY Magneto Bench Tester for Slick (4300/6300 series) and Bendix (S-20/S-200 series) aircraft magnetos. Follow `safety_guidelines.md` to avoid electrical shock, mechanical injury, or fire. Complete `assembly_instructions.md` before proceeding.

## Tools Required
- Multimeter (for voltage and continuity)
- Feeler gauge (for spark gap adjustment)
- Reference tachometer (e.g., handheld optical tachometer)
- Insulated gloves and safety glasses
- Non-conductive probe (for spark gap testing)
- Stopwatch or timer

## Calibration Steps
1. **Verify Grounding**:
   - Use a multimeter to check continuity between the frame, motor, spark gap enclosure, and AC power ground.
   - Ensure the magneto’s P-lead is connected to the kill switch and grounded when activated.
   - Confirm no exposed high-voltage terminals are accessible.

2. **Calibrate the Digital Tachometer**:
   - Attach a reflective strip to the motor shaft or pulley.
   - Power on the tester and set the PWM controller to 50% speed.
   - Compare the tester’s digital tachometer reading to a reference tachometer aimed at the reflective strip.
   - Adjust the tachometer’s calibration settings (if applicable, per its manual) to match the reference within ±10 RPM.
   - Test at 500, 1500, and 3000 RPM to ensure accuracy across the range.

3. **Set Spark Gap Width**:
   - Open the spark gap enclosure (power off, P-lead grounded).
   - Use a feeler gauge to set each spark plug gap to 5-7mm (consult magneto manual for model-specific recommendations).
   - Tighten spark plugs securely in the enclosure to prevent vibration.

4. **Check Electrical Connections**:
   - Inspect all wiring for secure connections and proper insulation (600V-rated for power/control, 10kV silicone for HT leads).
   - Verify the 15A fuse (AC input) and 10A fuse (DC motor circuit) are intact.
   - Test the emergency stop button: power on, press the button, and confirm motor stops and P-lead grounds.
   - Test the kill switch: activate and confirm no spark output at the spark gaps.

## Testing Procedures
1. **Initial Power-On Test**:
   - Follow the pre-operation checklist in `safety_guidelines.md`.
   - Connect the tester to a 120V AC GFCI outlet.
   - Turn on the master toggle switch and confirm the LED indicator lights.
   - Gradually increase the PWM controller to 500 RPM and verify smooth motor operation with no excessive vibration.

2. **Magneto Installation and Spark Test**:
   - Mount a Slick or Bendix magneto on the universal plate (per `assembly_instructions.md`).
   - Connect the magneto’s HT leads to the spark gap array’s terminal block.
   - Set the PWM controller to 500 RPM and observe spark consistency across all gaps.
   - Increase to 1500 RPM (typical coming-in speed) and confirm stable sparking.
   - Use a non-conductive probe to check for stray sparks outside the gaps (indicating insulation issues).
   - Activate the kill switch and verify all sparking stops instantly.

3. **Coming-In Speed Verification**:
   - Gradually reduce RPM from 1500 to 0, noting the RPM at which sparking begins (coming-in speed, typically 150-300 RPM for healthy magnetos).
   - Compare to the magneto’s specification (consult manufacturer documentation).
   - Repeat three times to ensure consistency within ±20 RPM.

4. **High-Speed Test**:
   - Increase to 3000 RPM (maximum operating speed) for 30 seconds.
   - Monitor for consistent sparking, stable RPM, and no overheating of the motor or PWM controller.
   - Check belt alignment and listen for abnormal noises (e.g., bearing wear, misalignment).

5. **Safety Feature Validation**:
   - Test the emergency stop button at 1500 RPM: press and confirm immediate motor shutdown and P-lead grounding.
   - Verify guards around belts/pulleys are secure and warning labels are visible.
   - Ensure the spark gap enclosure is ventilated and ozone levels remain low (no strong odor).

## Pass/Fail Criteria
- **Tachometer Accuracy**: Within ±10 RPM of reference tachometer at 500, 1500, and 3000 RPM.
- **Spark Consistency**: All spark gaps produce strong, consistent sparks at 500-3000 RPM.
- **Coming-In Speed**: Within manufacturer’s specified range (±20 RPM).
- **Safety Systems**: Emergency stop and kill switch function instantly; grounding is continuous.
- **Mechanical Stability**: No excessive vibration, misalignment, or loose components.

## Troubleshooting
- **Inconsistent Sparks**: Check HT lead connections, spark gap width, or magneto condition. Replace faulty spark plugs.
- **Tachometer Error**: Re-calibrate or replace the reflective strip. Verify sensor alignment.
- **Motor Vibration**: Re-align pulleys, tighten bolts, or replace worn belts.
- **No Spark Output**: Confirm P-lead is not grounded, check kill switch wiring, or test magneto separately.

## Post-Testing Checklist
- Follow the post-operation checklist in `safety_guidelines.md`.
- Document test results (RPM, spark quality, coming-in speed) in a log.
- Inspect components for wear or damage and update `docs/bill_of_materials/parts_list.csv` if replacements are needed.

## Notes
- **Safety First**: Wear insulated gloves and safety glasses during testing. Never touch HT leads or spark gaps while powered.
- **Documentation**: Record calibration data and photos in `docs/photos/test_results/`.
- **Professional Verification**: For aviation-critical use, have the magneto certified by an FAA-approved repair station.

**WARNING**: Improper calibration or testing can lead to false results or hazards. Consult an A&P mechanic if unsure. Refer to `safety_guidelines.md` for all safety protocols.