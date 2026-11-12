Hello , Welcome to this forked Germinal repo to work on UAI servers

a couple notes:

When you want to target new residues, you must create a new .yaml file in the /target/ file . Follow the same format as the other .yaml files but chagne the amino acids being targetted. Be sure to name it ending in .yaml 

I have added two HRU home grown frameworks sequences: Losizumab and Ahanizumab (note* these are not real drugs). Both are loosely based on caplacuziman with a couple residue changes to suit our requirements. Below are the sequences and framework lengths. It is best when using these frameworks to change the cdr and fw lengths to these values. although it is not necessary:

Losizumab: EVQLVESGGGLVQPGGSLRLSCAASGRTFSYNPMGWFRQAPGKGRELVAAISRTGGSTYYPDSVEGRFTISRDNAKRMVYLQMNSLRAEDTAVYYCAAAGVRAEDGRVRTLPSEFDYWGQGTQVTVSS cdr_lengths: [11, 8, 5]
fw_lengths: [25, 17, 40, 17]

Ahanizumab
cdr_lengths: [11, 8, 5]
fw_lengths: [25, 17, 40, 17]

Separatley:
Vhh.yaml file found in /run/ is where all changes take place and you can define the framework pdb and cdr/fw lengths. It is best to stick loosely to the cdr/fw lengths of the framework you are using , but not completely neccessary. Below are the available frameworks, their sequence, and cdr/fw regions

Caplacizumab:
cdr_lengths: [11, 8, 10]
fw_lengths: [25, 17, 38, 14]

Caplacizumab_kinked:

Vobarilizumab:

nb: 

I recommend only using these frameworks (+Losizumab and Ahanizumab)

Happy Designing!
