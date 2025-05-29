cat > docs/build_guide/assembly_instructions.md << EOL
# Assembly Instructions for DIY Magneto Bench Tester

This guide provides step-by-step instructions for assembling the DIY Magneto Bench Tester for Slick (4300/6300 series) and Bendix (S-20/S-200 series) aircraft magnetos. Follow \`safety_guidelines.md\` at all times to avoid electrical or mechanical hazards.

## Tools Required
- Wrenches and screwdrivers (standard and insulated)
- Drill and bits for metal
- Multimeter for continuity and voltage testing
- Soldering iron and solder (for electrical connections)
- Wire strippers and crimpers
- Measuring tools (caliper, ruler, feeler gauge)
- Safety glasses and insulated gloves

## Components
Refer to \`docs/bill_of_materials/parts_list.csv\` for the complete list of components, including the DC motor, PWM controller, spark plugs, and enclosure materials.

## Assembly Steps
1. **Build the Frame**:
   - Cut steel angle iron (1.5in x 1.5in x 1/8in) to form a rectangular base (e.g., 24in x 12in).
   - Weld or bolt the frame together, ensuring stability.
   - Mount rubber isolation mounts to the frame base to reduce vibration.
   - Secure the frame to a workbench with bolts.

2. **Install the Motor and Drive System**:
   - Mount the 1/2 HP DC motor to the frame using bolts and rubber mounts.
   - Attach a timing pulley to the motor shaft (5/8” or 3/4” bore).
   - Install a matching pulley on the magneto drive shaft adapter.
   - Connect pulleys with a toothed timing belt (e.g., Gates 5M150).
   - Verify alignment with a straightedge or laser tool to prevent belt wear.

3. **Fabricate the Magneto Mounting Plate**:
   - Cut a 1/4in aluminum plate (12in x 12in) to fit Slick and Bendix magneto bases.
   - Drill multiple bolt patterns for universal compatibility (refer to magneto manuals for dimensions).
   - Attach the plate to the frame with bolts, ensuring alignment with the motor pulley.
   - Add rubber pads under the plate for vibration damping.

4. **Assemble the Spark Gap Array**:
   - Mount 6 automotive spark plugs (e.g., NGK BKR5E) in a polycarbonate enclosure (1/4in thick, 12in x 12in).
   - Set gaps to 5-7mm using a feeler gauge.
   - Connect each spark plug to an insulated terminal block for HT lead attachment.
   - Ground one electrode of each spark plug to the frame.
   - Add ventilation holes to the enclosure to manage ozone.

5. **Wire the Electrical System**:
   - Connect the 120V AC input to a 15A fuse holder and master toggle switch with an LED indicator.
   - Wire a 12V/24V DC power supply to the PWM controller and motor.
   - Install a 10A fuse for the motor circuit.
   - Connect the digital tachometer (optical or Hall-effect sensor) to the motor shaft.
   - Wire the momentary kill switch to the magneto’s P-lead and ground.
   - Install the emergency stop button to cut motor power and ground the magneto.
   - Use 14-18 AWG wire (600V-rated) for power/control and 10kV silicone wire for HT leads.
   - Secure wires with cable ties and route away from rotating parts.

6. **Add Safety Features**:
   - Attach guards around belts and pulleys (metal or polycarbonate).
   - Affix “DANGER: HIGH VOLTAGE” and “WARNING: ROTATING PARTS” labels near the spark gap and drive system.
   - Verify ground continuity with a multimeter.

7. **Test the Assembly**:
   - Follow \`calibration_and_testing.md\` to verify RPM accuracy, kill switch functionality, and spark consistency.
   - Check for loose connections, vibrations, or alignment issues.

## Notes
- **Precision**: Ensure all mechanical alignments are within 0.01in to prevent wear.
- **Safety**: Test the emergency stop and kill switch before powering on.
- **Documentation**: Take photos during assembly and store them in \`docs/photos/build_process/\`.

## Next Steps
- Calibrate the tester as per \`calibration_and_testing.md\`.
- Refer to \`operation_manual.md\` for operating instructions.
- Update \`docs/bill_of_materials/parts_list.csv\` with any substitutions.

**WARNING**: Follow \`safety_guidelines.md\` to avoid electrical shock, mechanical injury, or fire. Consult an A&P mechanic if unsure about any step.
EOL
git add docs/build_guide/assembly_instructions.md
git commit -m "Add assembly_instructions.md with construction steps"
git push