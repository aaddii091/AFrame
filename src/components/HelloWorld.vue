<template>
  <a-scene>
    <a-assets timeout="10000">
      <img id="city" src="../assets/2.jpg" />
      <!-- <a-asset-item
        id="tree"
        src="../assets/EDV.gltf"
        timeout="10000"
      ></a-asset-item> -->
      <img id="my-image" src="../assets/2397715.jpg" />
    </a-assets>
    <a-box position="-1 0.5 -3" rotation="0 45 0" color="#4CC3D9"></a-box>
    <a-sphere position="0 1.25 -5" radius="1.25" color="#EF2D5E"></a-sphere>
    <a-cylinder
      position="1 0.75 -3"
      radius="0.5"
      height="1.5"
      color="#FFC65D"
    ></a-cylinder>
    <a-plane
      position="0 0 -4"
      rotation="-90 0 0"
      width="10"
      height="10"
      color="#43C877"
    ></a-plane>

    <a-entity
      rotation="0 0 0"
      animation="property: rotation; to: 0 360 0; loop: true; dur: 10000  easing: linear;"
      position="0 -13 0"
      scale="0.5 0.5 0.5"
      gltf-model="https://jeromegraves.com/assets/elephant.glb"
    >
    </a-entity>
    <a-entity
      position="0 13 0"
      rotation="0 0 0"
      scale="0.5 0.5 0.5"
      gltf-model="../assets/EDV.gltf"
    >
    </a-entity>

    <a-curvedimage
      src="#my-image"
      height="3.0"
      radius="5.7"
      theta-length="72"
      rotation="0 100 0"
      position="1 4 0"
      scale="1 1 1"
    ></a-curvedimage>
    <a-sky id="image-360" radius="100" src="#city"></a-sky>

    <a-camera
      wasd-controls="acceleration:100"
      position="0 1.6 0"
      fly="true"
      enabled="true"
    ></a-camera>
  </a-scene>
</template>

<script>
import "aframe";
export default {};
</script>

<style>
a-scene {
  height: 500px;
  width: 100%;
}
</style>
