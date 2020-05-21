#### THREEJS + MaptasticJS Template

My starter template for anything 3d and video mapping.  Project [Three.js](https://threejs.org) onto stuff with [maptastic](https://github.com/glowbox/maptasticjs)! 

#### WHY

ThreeJS is amazing, projection mapping is fun.  So is live-coding it.  Why not?

#### SETUP

Requirements:

```
* git
* node v13.70 and up
* A modern browser (latest Chrome/FF)
* A WebGL-enabled video card (probably most will work)
```

If the above checks, then do the following

```
git clone https://github.com/mikebelanger/threejs_maptastic_template.git
cd threejs_maptastic_template
npm install
node server.js
```

#### USING

Open up `localhost:5000`.  You should see a single green cube.  Use Shift + Space to toggle Maptastic to drag the corners.  Hit "F" to get into fullscreen.  Hit Esc to get out.

To get something moving, open the browser console in a separate window, and enter this:

```
var animate = function () {
	requestAnimationFrame( animate );
	
	// wrap the 'moving' stuff in try, so if 
	// you mess up live, things keep going
	try {
		cube.rotation.x -= 0.01;
		cube.rotation.y += 0.0001;
		
		cube.position.setX(1)
    
	} catch(e) {
		console.log(e)
		
	}
	
	renderer.render( scene, camera );
};

animate()
```

Try changing the code within the try block, see if you can change other variables over time.  Kinda fun.

Tip: If you're using Firefox, try [using multi-line mode](https://hacks.mozilla.org/2019/12/firefox-71-a-year-end-arrival/) and enter/modify the above code there.   On OSX its Command+Enter to reload the console code.

#### FEEDBACK

Please open any issues you may have.  This is just a starter template, not really aiming to add other features.