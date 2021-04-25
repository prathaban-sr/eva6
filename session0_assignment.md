### 1. What are Channels and Kernels (according to EVA)? ###

A channel is a container for same kind of information. e.g. All digital images are formed using a
combination of RGB colors. Red, Green and Blue are individual channels of information. For print
medium, there are four separate channels of information, CMYK.
When we are looking at identifying more specific objects like text information, each alphabet can be
considered as a channel. Say, the letter e, written in multiple fonts, sizes, orientation, case can be
grouped into one channel. The accuracy obtained by defining channels at this level may not be great. We
can improve the accuracy of the model further by creating channels for each font/size/case/orientation of
e.
These channels identified by the first layer in the network, can be used to compose more complex
channels in subsequent layers. This is the core concept of how a human vision system works and how
neural networks have been modelled to work as well.
Kernels are also referred to as filters or feature extractors. In a physical sense, kernels are matrices of
size 3*3, 5*5 etc. They get convolved with the pixels in the image to extract features and form the next
layer.

### 2. Why should we (nearly) always use 3x3 kernels? ###

As the number of layers grows, a major concern is to keep the number of parameters to the
minimum required. Convolutions have the property that multiple convolutions with a small matrix
can be equivalent to a single convolution with a large matrix. e.g. A single convolution with a 7*7
matrix is the same as 3 convolutions with a 3*3 matrix. The number of parameters used in a 7*7
matrix is 49 but the number of parameters used in 3 convolutions using 3*3 matrix is 27. Due to
this advantage of keeping the number of parameters low, 3*3 kernels are preferred in many
scenarios.

### How many times do we need to perform 3x3 convolutions operations to reach
close to 1x1 from 199x199 (type each layer output like 199x199 > 197x197...) ###

We need to perform the convolution 99 times.

*	199	*	199	>	197	*	197
*	197	*	197	>	195	*	195
*	195	*	195	>	193	*	193
*	193	*	193	>	191	*	191
*	191	*	191	>	189	*	189
*	189	*	189	>	187	*	187
*	187	*	187	>	185	*	185
*	185	*	185	>	183	*	183
*	183	*	183	>	181	*	181
*	181	*	181	>	179	*	179
*	179	*	179	>	177	*	177
*	177	*	177	>	175	*	175
*	175	*	175	>	173	*	173
*	173	*	173	>	171	*	171
*	171	*	171	>	169	*	169
*	169	*	169	>	167	*	167
*	167	*	167	>	165	*	165
*	165	*	165	>	163	*	163
*	163	*	163	>	161	*	161
*	161	*	161	>	159	*	159
*	159	*	159	>	157	*	157
*	157	*	157	>	155	*	155
*	155	*	155	>	153	*	153
*	153	*	153	>	151	*	151
*	151	*	151	>	149	*	149
*	149	*	149	>	147	*	147
*	147	*	147	>	145	*	145
*	145	*	145	>	143	*	143
*	143	*	143	>	141	*	141
*	141	*	141	>	139	*	139
*	139	*	139	>	137	*	137
*	137	*	137	>	135	*	135
*	135	*	135	>	133	*	133
*	133	*	133	>	131	*	131
*	131	*	131	>	129	*	129
*	129	*	129	>	127	*	127
*	127	*	127	>	125	*	125
*	125	*	125	>	123	*	123
*	123	*	123	>	121	*	121
*	121	*	121	>	119	*	119
*	119	*	119	>	117	*	117
*	117	*	117	>	115	*	115
*	115	*	115	>	113	*	113
*	113	*	113	>	111	*	111
*	111	*	111	>	109	*	109
*	109	*	109	>	107	*	107
*	107	*	107	>	105	*	105
*	105	*	105	>	103	*	103
*	103	*	103	>	101	*	101
*	101	*	101	>	99	*	99
*	99	*	99	>	97	*	97
*	97	*	97	>	95	*	95
*	95	*	95	>	93	*	93
*	93	*	93	>	91	*	91
*	91	*	91	>	89	*	89
*	89	*	89	>	87	*	87
*	87	*	87	>	85	*	85
*	85	*	85	>	83	*	83
*	83	*	83	>	81	*	81
*	81	*	81	>	79	*	79
*	79	*	79	>	77	*	77
*	77	*	77	>	75	*	75
*	75	*	75	>	73	*	73
*	73	*	73	>	71	*	71
*	71	*	71	>	69	*	69
*	69	*	69	>	67	*	67
*	67	*	67	>	65	*	65
*	65	*	65	>	63	*	63
*	63	*	63	>	61	*	61
*	61	*	61	>	59	*	59
*	59	*	59	>	57	*	57
*	57	*	57	>	55	*	55
*	55	*	55	>	53	*	53
*	53	*	53	>	51	*	51
*	51	*	51	>	49	*	49
*	49	*	49	>	47	*	47
*	47	*	47	>	45	*	45
*	45	*	45	>	43	*	43
*	43	*	43	>	41	*	41
*	41	*	41	>	39	*	39
*	39	*	39	>	37	*	37
*	37	*	37	>	35	*	35
*	35	*	35	>	33	*	33
*	33	*	33	>	31	*	31
*	31	*	31	>	29	*	29
*	29	*	29	>	27	*	27
*	27	*	27	>	25	*	25
*	25	*	25	>	23	*	23
*	23	*	23	>	21	*	21
*	21	*	21	>	19	*	19
*	19	*	19	>	17	*	17
*	17	*	17	>	15	*	15
*	15	*	15	>	13	*	13
*	13	*	13	>	11	*	11
*	11	*	11	>	9	*	9
*	9	*	9	>	7	*	7
*	7	*	7	>	5	*	5
*	5	*	5	>	3	*	3
*	3	*	3	>	1	*	1

### 4. How are kernels initialized? ###

Kernel initialization is generally done randomly, for starters. As the network trains the kernel values are updated. Due to this,
the features found in an individual neuron may vary from one training run to another but the same set of features should be extracted overall.

In scenarios where we are not getting the desired results, other initialization schemes like He initialization, MSRA initialization , Xavier initialization/Glorot initialization can be tried. 

### 5. What happens during the training of a DNN? ###
