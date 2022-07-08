This is a paper of type 1. Section 2 (p. 4-5) gives spectra per compound, including 195Pt, for example:

    (dppbe)Pt(2-diferrocenylthioketone) 3a. Orange colored crystals, yield: 61 mg (91%).1H (CD2Cl2, 400
    MHz): 7.75 (m, 1H, dppbe), 7.65 (m, 5H, dppbe), 7.47 (m, 2H, dppbe), 7.39 (m, 6H, dppbe), 7.33 (m,
    2H, dppbe), 7.23 (m, 8H, dppbe), 3.92 (m, 12H, 10H C5H5 and 2H C5H4), 3.85 (m, 2H, C5H4), 3.82 (m,
    2H, C5H4), 3.75 (m, 2H, C5H4).13C{1H} (101 MHz, CD2Cl2): 134.1 (m) 133.9 (m), 133.6 (m), 133.1 (m),
    132.7 (m), 131.8 (m), 131.2 (m), 130.6 (m), 130.2 (m), 128.9 (m), 128.6 (m), 102.9 (m, S=CFc2), 70.3 (m),
    69.7 (m), 69.4 (s, C5H5), 69.3 (m), 66.5 (s (C5H4), 66.3 (s, C5H4).31P{1H} NMR (CD2Cl2,162 MHz): 42.79 (d
    with 195Pt sat., 1JPPt = 2835.0, 2JPP = 28.1 Hz), 36.52 (d with 195Pt sat., 1JPPt = 4167.2, 2JPP = 28.0 Hz).
    195Pt{1H} (CD2Cl2, 129 MHz): -5059 (dd, 1JPtP = 4168 Hz, 1JPtP = 2835 MHz). ESI-MS(+mode) m/z: 1054.8 [M-2H]+
    (including isotope pattern as calculated). EA: C51H42Fe2P2PtS?0.5 toluene?0.25 pentane (calc./found):
    C: 59.80/59.71; H: 4.41/4.40; S: 2.86/2.65.
    
Identifying those section should be possible by them having the bold number after a chemical name and then the 1H, 13C, 195Pt sections with the shifts. 

From that section, we would need
1. The structure number
2. The 195Pt shift (?5059)
3. Additionally, the chemical name (dppbe)Pt(2-diferrocenylthioketone), solvent CD2Cl2, spectrometer frequency 129, and peak multiplicity dd would be useful.

This becomes a CML block like this:

    <spectrum moleculeRef="3d" type="NMR" xmlns:nmr="http://www.nmrshiftdb.org/dict" xmlns:siUnits="http://www.xml-cml.org/units/siUnits" xmlns:cmlDict="http://www.xml-cml.org/dict/cmlDict" xmlns:cml="http://www.xml-cml.org/dict/cml" xmlns:macie="http://www.xml-cml.org/dict/macie" xmlns:subst="http://www.xml-cml.org/dict/substDict" xmlns:units="http://www.xml-cml.org/units/units">
     <conditionList>
      <scalar dataType="xsd:string" dictRef="cml:field" units="siUnits:megahertz">129</scalar>
     </conditionList>
     <metadataList>
      <metadata name="nmr:OBSERVENUCLEUS" content="195Pt"/>
     </metadataList>
     <substanceList>
      <substance dictRef="cml:solvent" role="subst:solvent" title="CD2Cl2"/>
     </substanceList>
     <peakList>
      <peak xValue="-4899" xUnits="units:ppm" peakMultiplicity="dd" id="p0" atomRefs="a1"/>
     </peakList>
    </spectrum>

The structure, identified by bold number 3a, is in Figure 2 on page 4. This needs to be converted to CML. Figures can be identified by having the bold numbers in them (perhaps the captions help as  well, but the bold numbers seem a very reliable sign).

With all structures and spectra, this would become a CML file like spectra.cml in this folder. It has all structures, with the number as ID, and a spectrum for each. It also has the literature reference in bibtexml, but that is not crucial as long as the literature item can be found (including the PMC id would do).
