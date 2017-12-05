# Medical-Image-Modality-Conversion


Observations and improvement:

1. there are still significant amount of noisy images in the dataset, which led to some of the inference to be noisy. Noisy images include:
1. images that contain mostly just noise, 
2. images that don't have representation power - those part of brian slices that are simply to small to infer knowledge from, 
3. images that have republicating objects/shade,
4. images that contains a lot of noise in the background but seems to have ok amount of information on brain.

need to really clean up the dataset

Technique issues to tackle with:

1. quality of conversion: overall, the results are encouraging in the sense that you can see the parts that usually light up in T2 to light up in T1-T2 conversion. On a high level knowldge, the conversion is decent; however, closer inspection shows a few problems: first, details are not well preserved - which is partially due to noisy input, and partially due to the fact that we are extracting high level features in order to perform this kind of transformation. Secondly, some interpretations by computers are obviously wrong - for instance, the model would 'intepretate' a tumor as part of the brain structure, and after conversion, it looks like part of the brain instead of a tumor. 

2. Spatial consistency - this needs to be updated after i run some more data through the model. I am assuming that spatially it is not very consistent. We will need to come up with a constraint in this axis.

Posssible solution:

1. We can get spatial consistency from https://arxiv.org/abs/1604.08610

2. We can probably get an increase in performance by categorizing the brain parts first - similar approaches have been applied in the face conversion domain, where the fudicial points were first recognized and the constraints are put on them to be consistent. We need to look into existing models/github code that can readily extract information from MRI, e.g. where is frontal cortex, and approximately in what position of the brain.



