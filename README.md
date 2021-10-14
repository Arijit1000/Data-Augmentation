**Applying the same augmentation with the same parameters to multiple images, masks, bounding boxes, or keypoints

Sometimes we want to apply the same set of augmentations to multiple input objects of the same type. For example, you might have a set of frames from the video, and you want to augment them in the same way. Or you may have multiple masks for the same image, and you want to apply the same augmentation for all of them.

In Albumentations, we can declare additional targets and their types using the additional_targets argument to Compose.

For the name of an additional target, we can use any string value that is also a valid argument name in Python. Later, we will use those names to pass additional targets to a transformation pipeline. So we can't use a string that starts with a digit, such as '0image' because it is not a valid Python argument name.

The type could be either image, mask, bboxes, or keypoints.
