# Lab Automation Tools
This is a work in progress and there are more iterations/improvements to come. Any suggestions would be much appreciated. 

I designed these programs for our lab's needs, it works for us. It may not work for everyone or may take optimization to work. We mainly sequence bacteria and mycology samples. This has not yet been tested on gDNA from cell lines or ultra-HMW samples.
## Eppendorf EpMotion 5075 tube-to-plate and normalization
Is your sample in a tube? would you like it in a 96-well plate? Then the tube-to-plate protocol is for you.

So your sample is now in a 96-well plate. Lets normalize it! Using the ONT_Normalization excel doc place your sample concentrations in the first table. Save the Sample_CSV tab as a CSV and Water_CSV as a separate CSV. Now open the normalization program on your EpMotion and import these CSVs. 

## Eppendorf EpMotion 5075 Library Preparation of gDNA using Oxford Nanopore LSK109 with Native barcoding
The protocol is designed to process 24 samples and breaks it into 2 programs: end-prep and native barcoding.
-If you'd like to edit this to work with more/less samples don't forget to edit the barcoding incubation wait time as well. 

We multiplex 8 samples/flowcell. If you'd like to multiplex more you'll need to edit the barcode reagent transfer step. 

I recommend 500-2000ng of starting material. 

1000f tips are used as we have a surplus of these and 300f tips are harder to come by.

I have not been able to resuspend SPRI beads after the bead cleanup in the end-prep program. I stop the program, seal the plate, and place it on a shaker at low speed. 

Blunt TA and barcodes need to first be placed in a plate before being placed on the deck. This is to reduce the time it takes to add Blunt TA. 

I resuspend my final barcoded libraries in 15ul to concentrate them; however, any amount higher will work fine. I haven't tested lower volumes. 

In line with the coming SQK-NBD112.96 kit I plan on combining the end-prep and barcoding protocols into one, with a single bead cleanup. This will hopefully increase recovery.

Final pooling, adapter ligation, and loading are still done by hand. 

Thank you,
Sam
