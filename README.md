# Lab Automation Tools
This is a work in progress and there are more iterations/improvements to come. Any suggestions would be much appreciated. Please feel free to contact me with questions, concerns, and ideas at sgreenfield@atcc.org

I designed these programs for our lab's needs, it works for us. It may not work for everyone or may take optimization to work. We mainly do WGS sequencing on bacteria and mycology samples. This has not yet been tested on gDNA from cell lines or ultra-HMW samples.
## Eppendorf epMotion 5075 Library Preparation of gDNA using Oxford Nanopore’s SQK-NBD114.96, Native Barcoding Kit 96 V14.
This is the long awaited update to my previous protocols! It is fully walk away and combines both the end-prep and barcode ligation. 

Our protocol is designed for up to 64 samples with 8 samples/pool and differs from ONT’s program. The ONT program only works if you’re multiplexing enough samples together in one run. The program here is designed for lower multiplexed samples, in our case 8. 
Surface teaching is required before this program can be run!

We’re still waiting on the 114 kits to be fully released before using them. For now we’re using the EXP-NBD196 barcoding kit and transferring the volume we need into a PCR plate. 
The starting input needs to be uniform across all samples that are being multiplexed together until ONT’s barcode balancing is fully released. We input 128ng/sample in 25.6 uL (5.0ng/uL)
To calculate the amount of end-prep master mix needed do the following:
1.	Multiply the minimum by 9. This will give you your total volume. 
2.	Multiply the total by 0.29 to find the volume of both FFPE and Ultra II buffer needed. 
3.	Multiply the total by 0.25 to find the volume of Ultra II mix needed. 
4.	Multiply the total by 0.16 to find the volume of FFPE mix needed. 

We use 0.5M EDTA pH 8.0.

The Blunt TA needs to be kept cold until use. Place the ReservoirRack Module TC in the freezer at least an hour before starting this protocol. Better yet always store the module in the freezer. 

Use Thermo Scientific Deepwell plates catalog no. 278606. During initialization it will always throw an error while checking this plate. Select ignore and allow the initialization to keep going. 

The program will do a cleanup of 8 pools regardless of how many samples you input. The sample input will however change the minimum volumes of reagents. If you’re multiplexing more than 8 samples you’ll need to edit steps 26 and 30. This program could also be changed to work with 96 samples by changing from 1 column of pooled cleanups to 2. You’ll also need to add a second empty vessel command for the second column. 

Adapter ligation and loading are still done by hand.

Thank you,

Sam 
