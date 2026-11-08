# Setup and reproduction checklist

## Required environment

- HP 8903B audio analyzer and a compatible GPIB interface (the thesis background identifies GPIB-HS).
- LabVIEW compatible with the supplied VI files. The archive references LabVIEW 2023; binary metadata includes `23.1`. Exact version compatibility remains to be tested.
- Compatible NI-VISA/GPIB software and the HP8903B instrument-driver library, obtained under its applicable license.

## Suggested workflow (not executed during archive preparation)

1. Install the instrument driver so LabVIEW can resolve `<instrlib>/hp8903b/HP8903B.LLB`.
2. Discover the instrument in the installed hardware configuration utility and confirm its actual VISA resource address. Do not assume the address visible in the archived screenshot applies to another setup.
3. Open `labview/final.vi` as an initial inspection entry point. Resolve missing subVIs and inspect the block diagram before running; the name alone does not establish that it is the latest working revision.
4. Review safe input/source settings against the instrument documentation and connected equipment.
5. Verify initialization and one measurement before enabling repeated acquisition or plotting.
6. Record the VI revision, hardware, software versions, measurement mode, input conditions and any VISA error codes.
7. Compare against an appropriate reference before reporting accuracy or performance improvements.

## Known archive limitations

The supplied screenshots include a VISA Read error. Alternative VIs are retained without an asserted release order. Frequency labels in image filenames are ambiguous and must not be used as proven acquisition bandwidth. The original archives contain packaged third-party driver files; these were excluded from this review repository, as were NI DAQmx example files, local machine aliases, miscellaneous waveform images and an administrative requirements document.
