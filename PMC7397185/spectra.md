This is a paper of type 2. There is a table on page 7, giving structure numbers to be found in Scheme 2 and 3, and the shift. The table is this:

|Complex |Ox. State |delta Pt (ppm) 195Pt NMR |delta C (ppm) 13C NMR|
| ----------- | ----------- | ----------- | ----------- |
|1| +II| -4313| 125.1|
|2| +II| -3814| 138.2|
|3| +II| -3356| 154.7|
|4| +II| -3351| n.o.|
|5| +II| -3304| n.o.|
|6| +IV| -2196| n.o.|
|7| +IV| -2168| 113.4|

Identifying the table should be possible from the "delta 195Pt" in the header.

From this, we get structure number (e.g. 1) and shift (e.g. -4313). This would be in CML:

    <spectrum moleculeRef="1" type="NMR" xmlns:nmr="http://www.nmrshiftdb.org/dict" xmlns:siUnits="http://www.xml-cml.org/units/siUnits" xmlns:cmlDict="http://www.xml-cml.org/dict/cmlDict" xmlns:cml="http://www.xml-cml.org/dict/cml" xmlns:macie="http://www.xml-cml.org/dict/macie" xmlns:subst="http://www.xml-cml.org/dict/substDict" xmlns:units="http://www.xml-cml.org/units/units">
     <conditionList>
      <scalar dataType="xsd:string" dictRef="cml:field" units="siUnits:megahertz">600</scalar>
     </conditionList>
     <metadataList>
      <metadata name="nmr:OBSERVENUCLEUS" content="195Pt"/>
     </metadataList>
     <substanceList>
      <substance dictRef="cml:solvent" role="subst:solvent" title="D2O"/>
     </substanceList>
     <peakList>
      <peak xValue="-4313" xUnits="units:ppm" id="p0" atomRefs="a1"/>
     </peakList>
    </spectrum>

The solvent comes from the table caption, which says "external reference for 195Pt: H2PtCl6 in D2O: delta Pt = 0 ppm). The frequency could be derived from section 3, where it says "The HMQC 1H-195Pt spectra were recorded on a Bruker AVANCE 600 spectrometer", but that is not essential.

The structures are given in Scheme 2 and 3, identified by the bold numbers in the table. This needs to be converted to CML. The bold number in the scheme should be good for identification (perhaps the captions help as  well, but the bold numbers seem a very reliable sign).

With all structures and spectra, this would become a CML file like spectra.cml in this folder. It has all structures, with the number as ID, and a spectrum for each. It also has the literature reference in bibtexml, but that is not crucial as long as the literature item can be found (including the PMC id would do).