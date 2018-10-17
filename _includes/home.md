# Let’s build the metaverse together

### The Decentraland SDK provides everything you need to build interactive 3D content for Decentraland.

---

[BIG ICONS WITH LINKS]

- Installation guide
- Scene content
- Entity reference
- Sample scenes

---

## Quickstart guide

#### Install the CLI

To get started, install the Command Line Interface (CLI).

The CLI allows you to compile and preview your scene locally. After testing your scene locally, you can use the CLI to upload your content.

> **Note**: Install the following dependencies before you install the CLI:
>
> - [Node.js](https://github.com/decentraland/cli#nodejs-installation) (version 8)
> - [IPFS](https://dist.ipfs.io/#go-ipfs)
> - [Python 2.7.x](https://www.python.org/downloads/)

To install the CLI, run the following command in your command line tool of choice:

```bash
npm install -g decentraland
```

Read [Installation guide]({{ site.baseurl }}{% post_url /getting-started/2018-01-01-installation-guide %}) for more details about installing the CLI.

#### Create your first scene

Create a new scene by running the following code in an empty folder:

```bash
dcl init
```

Preview the 3D scene in your browser by running the following command in that same folder:

```bash
dcl start
```

Read more about the scene preview in [preview a scene]({{ site.baseurl }}{% post_url /getting-started/2018-01-04-preview-scene %})

#### Edit the scene

Open the `scene.tsx` file in your scene folder with the source code editor of your choice.

![](/images/media/landing_sample_code.png)

Change anything you want from this code, for example change the _x_ position of one of the entities. If you kept the preview running in a browser tab, you should now see the changes show in the preview.

Download this 3D model of an avocado from [Google Poly](https://poly.google.com) in _glTF_ format. [link](https://poly.google.com/view/cgLBGFfm5FU)

![](/images/media/landing_avocado_gltf.png)

Create a new folder under your scene’s directory named `/models`. Extract the downloaded files and place them all in that folder.

In your scene’s code, add the following line in between the other XML entities:

{% raw %}

```tsx
<gltf-model
  src="models/Avocado.gltf"
  position={{ x: 3, y: 0.75, z: 2 }}
  scale={10}
/>
```

{% endraw %}

Check your scene preview once again to see that the 3D model is now there too.

![](/images/media/landing_avocado_in_scene.png)

Read [coding-scenes]({{ site.baseurl }}{% post_url /getting-started/2018-01-02-coding-scenes %}) for a high-level understanding of how Decentraland scenes function. Check [scene-content]({{ site.baseurl }}{% post_url /development-guide/2018-01-21-scene-content %}) for specifics about how to add content to a scene.

## Scene examples

---

[screenshot][screenshot] [screenshot]

Door scene Hummingbird scene BlockDog

---

See [sample scenes]({{ site.baseurl }}{% post_url /examples/2018-01-08-sample-scenes %}) for more scene examples.
Also see [tutorials]({{ site.baseurl }}{% post_url /tutorials/2018-01-03-tutorials %}) for detailed instructions for building scenes like these.

## Other useful information

- [game design constraints]({{ site.baseurl }}{% post_url /design-experience/2018-01-08-design-games %})
- [typescrip tips]({{ site.baseurl }}{% post_url /development-guide/2018-01-08-typescript-tips %})
- [3D model consierations]({{ site.baseurl }}{% post_url /development-guide/2018-01-09-external-3d-models %})
- [scene limitations]({{ site.baseurl }}{% post_url /development-guide/2018-01-06-scene-limitations %})