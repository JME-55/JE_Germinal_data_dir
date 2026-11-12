Hello , Welcome to this forked Germinal repo to work on UAI servers

a couple notes:

When you want to target new residues, you must create a new .yaml file in the /target/ file . Follow the same format as the other .yaml files but chagne the amino acids being targetted. Be sure to name it ending in .yaml 

when changing the experiment name in the ipynb file in jupyter notebooks please use this consistent nomenclature : INITIALS_target_amino acids hotspot_framework_run number  eg JE_adamts7mpdis_A181_A184_A271_capla_1

I have added two HRU home grown frameworks sequences: Losizumab and Ahanizumab (note* these are not real drugs). Both are loosely based on caplacuziman with a couple residue changes to suit our requirements. Below are the sequences and framework lengths. It is best when using these frameworks to change the cdr and fw lengths to these values. although it is not necessary:



Losizumab, based on Caplacuzimab has the sequence changes incorporated:
cdr3 ntd 'AA'
cdr3 ctd 'FDY'
ctd 'SS'
Losizumab sequence: EVQLVESGGGLVQPGGSLRLSCAASGRTFSYNPMGWFRQAPGKGRELVAAISRTGGSTYYPDSVEGRFTISRDNAKRMVYLQMNSLRAEDTAVYYCAAAGVRAEDGRVRTLPSEFDYWGQGTQVTVSS Losizumab cdr_lengths: [11, 8, 5]
Losizumab fw_lengths: [25, 17, 40, 17]

Ahanizumab, based on Caplacuzimab has the amino acid sequence changes incorporated: 
cdr3 ntd 'AA'
cdr3 ctd 'YDY'
ctd 'SS'
Ahanizumab sequence: EVQLVESGGGLVQPGGSLRLSCAASGRTFSYNPMGWFRQAPGKGRELVAAISRTGGSTYYPDSVEGRFTISRDNAKRMVYLQMNSLRAEDTAVYYCAAAGVRAEDGRVRTLPSEYDYWGQGTQVTVSS
Ahanizumab cdr_lengths: [11, 8, 5]
Ahanizumab fw_lengths: [25, 17, 40, 17]



Separatley:
Vhh.yaml file found in /run/ is where all changes take place and you can define the framework pdb and cdr/fw lengths. It is best to stick loosely to the cdr/fw lengths of the framework you are using , but not completely neccessary. Below are the available frameworks, their sequence, and cdr/fw regions



Caplacizumab sequence: EVQLVESGGGLVQPGGSLRLSCAASGRTFSYNPMGWFRQAPGKGRELVAAISRTGGSTYYPDSVEGRFTISRDNAKRMVYLQMNSLRAEDTAVYYCAAAGVRAEDGRVRTLPSEYTFWGQGTQVTVSS
Caplacizumab cdr_lengths: [11, 8, 10]
Caplacizumab fw_lengths: [25, 17, 38, 14]

Caplacizumab_kinked:EVQLVESGGGLVQPGGSLRLSCAASXXXXXXXXXXWFRQAPGKGRELVAXXXXXXXXXXYPDSVEGRFTISRDNAKRMVYLQMNSLRAEDTAVYYCXXXXXXXXXXXXXWGQGTQVTVSS
Caplacizumab_kinked cdr_lengths: [10, 10, 13]
Caplacizumab_kinked fw_lengths: [25, 14, 37, 11]

Vobarilizumab:EVQLVESGGGLVQPGGSLRLSCAASXXXXXXXXXXWYRQAPGKGRELVAXXXXXXXXXYADSVKGRFTISRDNAKNTLYLQMNSLRPEDTAVYYCXXXXXXXXXWGQGTLVTVSS
Vobarilizumab cdr_lengths: [10, 9, 9]
Vobarilizumab fw_lengths: [25, 14, 37, 11]


I recommend only using these frameworks (+Losizumab and Ahanizumab)

Note: to submit jobs with a different framework you must do a slightly hacky method for germinal to use the correct frameowrk sequence. You have to copy and paste the atomic coordinate values found in each file and paste into and replace the scfv.pdb. Then change 'type' in the vhh.yaml to the name of your desired frameowrk. This is a bit long but should work. we are working with Miguel at ARC( who requires fundng) to change the germinal hardcode to make this process smoother. Alternatively If for any reason, defining these in the vhh.yaml doesnt work, select nb and change the nb sequence to the sequence you desire and define 'type'=nb. its longer, but it should work

Happy Designing! (12.11.26)
