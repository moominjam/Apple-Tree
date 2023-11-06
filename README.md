# Apple-Tree
The team's initial design files are in the libraries file

## Animation Brief 
Perlin noise can create changing clouds, flames, particle movement, and other naturally changing visual effects, so I chose to use Perlin noise to achieve the visual effect of randomly changing clouds and the sun.

By implementing the generation of random seeds, it provides the basis for the placement of each element and the rendering of the noisy background. Each time the page is refreshed, all the animation elements such as the sun halo, blue sky and white clouds background noise will produce subtle changes, resulting in a lively and bright visual effect.

### Animation of the sun
First, I created a dynamic noise cloud background, using random seed, and set the noiseSeed to take a random number before 0-999. By changing the value of zoff with the frameCount variable, the cloud morphology and motion is different each frame from the previous one, resulting in a landscape of clouds in constant motion across a blue sky.

### Blue sky and white cloud animation
The implementation of the sun animation also takes full advantage of the properties of Perlin noise. By adjusting the noise scaling factor to control the frequency and amplitude of the fluctuation, where frameCount*0.01 is used as the parameter of the noise function, the sun's halo shows a continuous and natural fluctuation effect. Each layer of the solar halo is fine-tuned with different Perlin noise values for rotation and transparency. When adjusting the transparency of the solar halo, the noise value is mapped to a range of 100 to 150, which means that the visibility of the halo appears to change slightly as the noise value fluctuates. It converts continuous noise values into discrete transparency changes for a more subtle and layered halo flicker effect. This use of the noise function not only provides multiple layers of visual depth to the sun halo but also makes the whole image livelier and brighter.

## Refresh page
Each time the page is refreshed, elements in the animation such as the clouds and the sun will look and behave differently due to the random seed change.

Even if the page is not refreshed, the Perlin noise function continues to animate the clouds and the sun so that they appear to be constantly changing dynamically, based on changes in parameters such as `frameCount`.
