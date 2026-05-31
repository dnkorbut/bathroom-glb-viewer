live demo: http://dnkorbut.com/luna/glb_webgpu.html
for webGL variant: http://dnkorbut.com/luna/glb_webgl.html

I have managed to implement all the passes except SSGI as it is too expensive and heavy task which would take more time to complete in an efficient way

webGL has SSGI out of the box but it needs to be set and I don't think it is the right solution for a viewer

with webGPU and I think with webGL as well we may consider writing a custom shader with a pre-baked scene instances to end up as efficient as possible

I used standard lib functions for AO which I think works well. But standard SSR needs to be combined with a pre-baked map and SSGI custom shader to make it reference-like

I've got 35-55 fps on macbook air M2 in google chrome. 35-50 for webGPU and 40-55 for webGL - which could be improved to be kept at no less than 50 with above constraints