## fuse-ios-camera-ux

This project is an attempt to learn and play with  [Fuse](http://www.fusetools.com/) by replicating the iOS stock camera app user interface.

Here's how far I got: [movie](./docs/fuse-ios-camera-ux-720p.mov).

My hope is that the video above is indistinguishable from the stock iOS camera app. It includes:
- [x] Mode switcher
- [x] UI responding to the various modes (record button, camera size, etc.)
- [x] Switch camera card flip
- [x] Controls (flash, hdr, etc.) functioning like the iOS controls do
- [x] All controls respond to orientation changes

## Installation

1. Clone this repo
2. Clone the two dependent repos
  - https://github.com/akalyan/fuse-camerapanel/tree/ak-observable-facing
  - https://github.com/akalyan/fuse-orientation
3. Fix the references to those dependencies in the fuse-ios-camera-ux.unoproj file
4. Build: `fuse build -t=ios -adebug`
5. Ensure only `Portrait` is selected in the General tab in XCode
6. Deploy to your device

## To Do

- [ ] Improve performance of switching the camera
- [ ] Reverse the backward-facing camera (it's currently [mirrored](https://github.com/bolav/fuse-camerapanel/issues/6))
- [ ] Improve app load experience (it's a bit jumpy when the camera stream loads)
- [ ] Fix landscape_left <-> portrait_down rotation (should rotate 90-deg, instead rotates -270-deg)
- [ ] Fix spacing of modes in carousel (spacing between TIME-LAPSE and SLO-MO is too small)
- [ ] Fix landscape layout of timer control when 3s or 10s are selected
- [ ] Add focus boxes
- [ ] Implement functionality to take and store a photo
- [ ] Implement functionality to take and store a video
- [ ] Migrate dependencies to [fusepm](https://github.com/bolav/fusepm)
