<template>
    <div ref="container" class="fixed inset-0 z-0"></div>
  </template>
  
  <script setup>
  import { onMounted, onBeforeUnmount, ref } from 'vue'
  import * as THREE from 'three'
  
  const container = ref(null)
  let scene, camera, renderer, stars = []
  let animationId
  
  onMounted(() => {
    initGalaxy()
    animate()
  })
  
  onBeforeUnmount(() => {
    cancelAnimationFrame(animationId)
    renderer?.dispose()
    window.removeEventListener('resize', onWindowResize)
  })
  
  function initGalaxy() {
    // Scene
    scene = new THREE.Scene()
  
    // Camera
    camera = new THREE.PerspectiveCamera(
      75,
      window.innerWidth / window.innerHeight,
      0.1,
      1000
    )
    camera.position.z = 1
  
    // Renderer
    renderer = new THREE.WebGLRenderer({ alpha: true }) // transparent
    renderer.setSize(window.innerWidth, window.innerHeight)
    container.value.appendChild(renderer.domElement)
  
    // Create stars
    const geometry = new THREE.BufferGeometry()
    const starCount = 10000
    const positions = []
  
    for (let i = 0; i < starCount; i++) {
      const x = THREE.MathUtils.randFloatSpread(2000)
      const y = THREE.MathUtils.randFloatSpread(2000)
      const z = THREE.MathUtils.randFloatSpread(2000)
      positions.push(x, y, z)
    }
  
    geometry.setAttribute('position', new THREE.Float32BufferAttribute(positions, 3))
  
    const material = new THREE.PointsMaterial({
      color: 0xffffff,
      size: 1,
      sizeAttenuation: true
    })
  
    const starsMesh = new THREE.Points(geometry, material)
    scene.add(starsMesh)
  
    window.addEventListener('resize', onWindowResize)
  }
  
  function onWindowResize() {
    camera.aspect = window.innerWidth / window.innerHeight
    camera.updateProjectionMatrix()
    renderer.setSize(window.innerWidth, window.innerHeight)
  }
  
  function animate() {
    animationId = requestAnimationFrame(animate)
  
    scene.rotation.y += 0.0005
    scene.rotation.x += 0.0002
  
    renderer.render(scene, camera)
  }
  </script>
  
  <style scoped>
  /* Makes sure the galaxy stays behind everything */
  canvas {
    position: absolute;
    top: 0;
    left: 0;
    z-index: 0;
  }
  </style>
  