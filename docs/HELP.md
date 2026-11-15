# Pixel Wrap 3D help

По-русски: [HELP.ru.md](HELP.ru.md)

## What the plugin does

Pixel Wrap 3D wraps a label or a logo around a 3D shape — a cylinder, a sphere, a cone or a body of revolution — and puts the result back into the document as a new layer. You match the shape to the object in the photo, so the label follows it with the right curve and perspective.

Only the label goes into the document. The shape, the grid and the markers are visible in the viewport alone.

## Quick start

1. Select the layer with the label or logo in the document and press **Use selected layer**. A regular layer, text and a smart object all work.
2. In the **Shape** group pick the shape closest to the object: **Cylinder**, **Sphere**, **Cone** or **Revolve**.
3. Match the shape to the object in the photo. The fastest way is the **Points** mode: put the markers on the axis and the edges of the object.
4. In the **Label** mode move the label to where it belongs on the shape.
5. Press **Apply** and answer the question about inserting — a new layer with the label appears in the document.

The next time you open the panel, the scene of the last Apply is restored by itself.

## Mouse modes

The buttons above the viewport choose what dragging does.

- **Shape** — Drag to move the shape over the document. Alt + wheel scales the shape.
- **Label** — Drag left-right and the label travels around the axis of the shape (that is **Rotation Y**); drag up-down and it moves along the axis. Alt + wheel scales the label.
- **Rotate** — Drag left-right for **Rotation Z**, up-down for **Rotation X**.
- **Points** — Fits the shape to markers on the photo — see the next section.
- **Contour** — The contour editor. The button shows only for a body of revolution.

In any mode: the wheel zooms the view, Space or the right button + drag pans it, **Fit** shows the whole document. Alt + drag switches to **Label** for the moment, Shift + drag to **Rotate**.

## Fitting by points

The fastest way to match the shape to the object. It works for a cylinder, a cone and a body of revolution.

1. Switch to the **Points** mode. Markers appear on the shape: square ones on the axis and round ones at the sides.
2. Put the square markers on the axis of the object: one at its start, the other at its end.
3. Set the width at each end with the round markers — on the edges of the object.
4. If the end face of the shape does not match the one in the photo, change **Field of view**: the points stay where they are and the shape re-fits to them.

The plugin works out the position, scale, rotations and length of the shape by itself; the perspective comes from how much smaller the far end of the object is than the near one. The radius of the shape can be changed with the points pinned, too. If the lines between the markers turn red, no shape can be built from these points and it stays as it was.

The mode is not available for a sphere or for a contour that closes to a point at an end. An orthographic camera shows no depth: the length of the shape is kept and its turn is worked out from how short the axis looks.

## Shape

- **Cylinder** — Set by **Radius** and **Height**.
- **Sphere** — Set by **Radius**.
- **Cone** — A truncated cone: **Top radius**, **Bottom radius** and **Height**.
- **Revolve** — A shape built from a contour you draw yourself: a bottle, a can, a vase.
- **Show shape** — Shows or hides the shape in the viewport.
- **Polygon grid** — A grid on the shape that makes its rotation and perspective easy to read. It works with the shape hidden as well.
- **Shape display** — **Fresnel** is a light fill with bright edges. **Solid** is a solid fill; the **Opacity** slider sets how dense it is.

## Contour editor

Opens with the **Edit contour** button or the **Contour** mode. You draw the right half of the silhouette over a snapshot of the document and the plugin revolves it around the axis.

- Click an empty spot for a new point; you can drag it straight away.
- Drag a point to move it. A double click makes it sharp or smooth; the **Sharp** and **Smooth** buttons do the same.
- Delete or the **Delete point** button removes the selected point.
- The square on the axis moves the axis, the circle at its end turns it.

The editor is flat: trace the silhouette as you see it and set the turn and the camera afterwards. A good contour can be kept in **Contour presets**: type a name and press **Save contour**.

## Shape position

- **X** and **Y** — The centre of the shape in document pixels.
- **Scale** — The size of the whole shape.
- **Rotation X** — Turns the top of the shape toward the viewer or away.
- **Rotation Y** — Turns the shape around its own axis: the label travels around it.
- **Rotation Z** — Turns the shape in the plane of the picture.

Every rotation is a full circle from 0 to 360°: after 360 comes 0, there are no stops.

## Label on shape

- **Along height** — Moves the label along the axis of the shape.
- **Rotation Z** — Turns the label itself on the surface: 90° lays it sideways, 180° turns it upside down.
- **Scale** — The size of the label.
- **Wrap angle** — How much of the circumference the label takes.
- **Keep label proportions** — Scale and wrap angle change together, so the label is not stretched.
- **Hide back side** — The part of the label that went behind the shape is not drawn.

The **Show label** switch at the top of the panel hides the label in the viewport while you match the shape. It does not affect the result.

## Camera and light

- **Perspective** — Near parts of the shape look larger than far ones, as in a photo. **Field of view** sets how strong the perspective is: the larger it is, the stronger.
- **Orthographic** — No perspective — for objects shot from far away.
- **Soft shading toward the shape edges** — The label darkens toward the edges of the shape; **Shading strength** sets by how much. Off by default: the colours of the layer are left alone.

## View and backdrop

- **Document backdrop** — How visible the document is under the shape in the viewport.
- **Show the source layer in the backdrop** — Shows the flat source layer in the backdrop. It usually gets in the way, so it is off.
- **Refresh backdrop** — Reads the document again if you changed it in Photoshop.
- **Reset parameters** — Puts the shape and the label back to the starting state.
- **Last applied parameters** — Brings back the parameters you last pressed **Apply** with.

## Number fields

- Type a number and press Enter.
- The up and down arrows change the value by one step, ten times faster with Shift.
- Drag the name of a field or the arrows icon left or right. Shift makes it faster, Alt finer.

## Inserting into the document

After you press **Apply** the plugin asks what to do with the label. The choice is remembered.

- **Multiply blend mode** — A dark label takes the light and shadow of the photo and stops looking like a sticker.
- **Blur by** — Blurs the label by the given number of pixels to match the sharpness of the photo, usually 1–3 px.

The result is a new layer exactly in place, on a transparent background, as a single step in Photoshop's history. The source layer is not changed. The result area is limited to 64 megapixels.

## Undo and redo

- Cmd+Z (Ctrl+Z) steps back, Shift+Cmd+Z or Ctrl+Y steps forward. The two arrows in the panel header do the same.
- One step is one finished action: a drag, a number, a change of shape.
- **Apply** is a step in Photoshop's own history. To undo the insert, click the document and press Cmd+Z there.

## Making the label look real

- For a dark label on a light object turn on **Multiply blend mode** when inserting.
- If the photo is softer than the label, turn on **Blur by**.
- If the edges of the object darken noticeably, turn on **Soft shading toward the shape edges**.
- A highlight over the ink is made in Photoshop itself: **Blending Options ▸ Blend If** — let the lightest tones of the underlying layer through.

## If something goes wrong

- **The plugin does not load** — Start Photoshop first, then press **Load** in UXP Developer Tools. After Photoshop restarts the plugin has to be loaded again.
- **The header shows the wrong version** — Use **Unload** and **Load**: after **Reload** Photoshop keeps the old manifest.
- **“No layer selected”, “Several layers are selected — select just one”** — Select exactly one layer in the Layers panel and press **Use selected layer**.
- **The document is not RGB** — The plugin works with RGB only: **Image ▸ Mode ▸ RGB Color**.
- **Another document is active** — Go back to the document the layer came from, or take the layer again.
- **The label disappeared** — It went to the back of the shape. Untick **Hide back side** or turn the shape: **Rotation Y** by 180°.
- **Cmd+Z does nothing** — Use the arrows in the panel header: Photoshop may catch the shortcut before the plugin does.
- **“The label is outside the document bounds”** — The shape is outside the document, or the whole label is on the back side.

Questions and bugs: pixmap1981@gmail.com or the Issues page at github.com/Toys-D/PixelWrap3D. Attach the lines from the UXP Developer Tools console that start with [Wrap3D].
