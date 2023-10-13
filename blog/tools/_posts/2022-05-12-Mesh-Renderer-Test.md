---
layout: post
title:  "Mesh Renderer Test"
date:   2022-05-12 14:11:00 +0900
description: >
  Testing
sitemap: false
hide_last_modified: true
---

test

const obj2gltf = require("obj2gltf");
const fs = require("fs");
const options = {
  binary: true,
};
obj2gltf("model.obj", options).then(function (glb) {
  fs.writeFileSync("model.glb", glb);
});