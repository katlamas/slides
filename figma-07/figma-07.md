---
theme: custom
paginate: true
marp: true
title: Figma - Week 6
---

# User Interactions, Transitions, and UI Component Design

---

## Prototypes

Prototypes are designs you can interact with.

In Figma, all prototypes start with a single interaction.

Each interaction consists of two parts: a **trigger** (what causes the interaction to start) and an **action** (the result of the trigger).

Some interactions take place on a single object, such as clicking on an object to open an external URL, or clicking a video to play and pause it.

Other interactions take place between two objects or frames, such as clicking a button to navigate to the next frame, or clicking an icon to open an overlay. 

---

These interactions are considered connections, which consists of three parts:

- **Hotspot**: A hotspot is where the interaction takes place. A hotspot can be the frame itself, or an object within the frame. You can create a hotspot on anything, like a button, icon, or heading.

- **Connection:** A connection is the arrow or "noodle" that connects the hotspot to the destination. Define the interaction trigger, actions, and adjust animation settings from the connection.

- **Destination:** The destination is where a connection ends. In most cases, the destination must be a top-level frame. Only connections using the Scroll to action can be set to a destination within the same top-level frame.

---

![bg contain](https://help.figma.com/hc/article_attachments/16943157833495)

---

## Add an interaction

An interaction is created by selecting a hotspot, or starting point.

1. Navigate to the **Prototype** tab of the right sidebar.

2. Select a layer or object for the interaction's hotspot.

3. Create the interaction by doing one of the following:
   
   - Hover over the object, and drag the plus icon to the destination frame

   - Click the **Add** in the **Interactions** section of the **Prototype** panel.

4. Once the interaction has been made, use the **Interaction details** panel to set the interaction trigger, action, and destination.

---

## Create interactions in bulk

You can create interactions from multiple objects at once. This can help you save time when creating multiple connections to the same destination.

1. Select your starting objects, or hotspots, where the interactions begin. You can select multiple objects via one of the following methods:
   
   - Select an initial object, then hold down Shift while clicking additional objects
   
   - Drag your cursor across any objects you want to select

---

2. Create the interactions by doing one of the following:
   
   - Hover over one of the selected objects, then click and drag the plus icon to the destination frame
   
   - Click the plus icon in the **Interactions** section of the **Prototype** panel, and use the Interaction details panel to set the trigger, action, and animation details

---

![bg contain](https://help.figma.com/hc/article_attachments/10786146173463)

---

## Interaction details

Once you create an interaction, use the **Interaction details modal** to configure the following:

**A.** **Trigger:** Defines what type of interaction will cause the prototype to advance forward, such as a mouse click or touch gesture.
**B.** **Action:** Defines what type of event happens when a user interacts with the hotspot, such as moving to another frame, or engaging an overlay.

---

**C.** **Destination:** Defines where the interaction ends. This could be another screen in the prototype, or an overlay that appears above the current screen. Not all interactions have destinations—for example, the Back trigger automatically returns to the previous frame.
**D.** **Animation settings:** Determine how the prototype moves from one frame to the other.
**E.** **State management:** Click to reset object properties and states when navigating in and across frames.
**F.** **Add action:** Add another action to the same trigger.
**G.** Close the **Interaction details** modal.

---

![bg contain](https://help.figma.com/hc/article_attachments/16944113988503)

---

A single object can have multiple interactions, each with its own trigger. For example, you might have an object with a video fill that has two interactions: One that plays the video **On click** and one that opens an overlay **When video ends**. 

A single object can have:

- Any number of the following triggers:
   - Key/Gamepad
   - On drag 
   - When video hits

---

- One of each of the following triggers:
   - On click / On tap
   - While hovering
   - While pressing
   - Mouse enter
   - Mouse leave
   - Mouse down / Touch press
   - Mouse up / Touch release
   - After delay
   - When video ends

---

## Adjust the animation

The animation settings determine how the prototype moves from one frame to the other.

**A.** **Animation:** The animation is how the prototype transitions from one frame to the next, such as push, slide, or dissolve.

**B.** **Direction:** For certain animation types (such as move in or push), you can set the direction controls which way you want the transition to move in. Choose between left, right, down, or up.

**C.** **Animate matching layers:** Check this box to apply the Smart animate transition to any matching layers.

---

**D.** **Easing and spring animation:** Easing determines the acceleration of the transition between a starting frame and its destination.

**E.** **Duration:** Duration controls how long it takes, in milliseconds (ms), to complete the transition. Choose a duration between 1ms and 10000ms (10 seconds).

**F.** Preview the animation.

---

![bg contain](https://help.figma.com/hc/article_attachments/16944254439703)

---

## Select and edit interactions

Use the tools below to improve and speed up prototype editing.

**Select matching interactions**

Matching interactions are identical interactions that begin from matching objects in other frames.

- **Identical interactions** are interactions with the same action and destination.

- **Matching objects** are objects in different frames that have identical names and matching hierarchy levels.

---

![bg contain](https://help.figma.com/hc/article_attachments/15940960531095)

---

To select matching interactions:

1. Select an interaction.

2. On the **Interaction details** modal, click **Select matching interactions**.

---

![bg contain](https://help.figma.com/hc/article_attachments/15940981804567)

---

Edit interaction details to update all selected interactions at once.

## Update connection destinations in bulk

If you have multiple connections, you can change the destination of those connections at the same time.

---

1. Select the connections you want to edit. You can select multiple connections via one of the following methods:
   
   - Select an initial connection, then hold down Shift while clicking additional connections.
   
   - Drag your cursor across any connections you want to select. This will create a blue box around the selected connections.

2. Hold and drag the connections to a new destination frame. You can also select the interaction from the right sidebar and change the destination frame from the Interaction details panel.

---

![bg contain](https://help.figma.com/hc/article_attachments/15941181950999)

---

## Copy and paste interaction details

Prototype faster by copying interaction details and pasting them on other objects.

1. Select a prototype interaction on the canvas.

2. Press ⌘ Command / Control + C to copy or ⌘ Command / Control + X to cut the interaction details.

3. Select another object on the canvas.

4. Press ⌘ Command / Control + V to paste the interaction details on to the new object.

---


## Create a loading animation in Figma

---

In this project, we’ll be making a loading animation. Adding loading animations can help your prototype look more realistic. If you follow along step-by-step, your final prototype will look like this:

![](https://help.figma.com/hc/article_attachments/24970044660759)

---

To achieve this design, we’ll do the following:

1. Create a frame and four ellipses

1. Duplicate the frame and rotate the ellipses

1. Duplicate the second frame and resize the ellipses

1. Add prototype connections

1. Create a component set

1. Add an instance to a new frame

---

## Create a frame and four ellipses

To start, select the Frame tool in the toolbar or press F and click on the canvas to add a frame with 100 x 100 dimensions. Double-click the frame name and rename it to “loading/1”.

We’ll make the animation pop by making the background dark. Select the frame and change the color to #000000 using the Fill setting in the right sidebar.

Now, let’s add four ellipses to the frame.

---

![bg contain](https://help.figma.com/hc/article_attachments/24794089080983)

---

1. From the Shape tools dropdown in the toolbar, select Ellipse or press O.

1. In the loading/1 frame, hold Shift and then click and drag your cursor to create a 24 x 24 ellipse.

1. Duplicate the ellipse and place it on the right side of the original ellipse. Use the red guides to help with the alignment.

1. Repeat the steps ‌until you have four ellipses in the frame. Place your ellipses in the ‌top-left, top-right, bottom-left, and bottom-right corners respectively.

1. Select the loading/1 frame and navigate to the Selection colors section in the right sidebar. Update the #D9D9D9 color to #FFFFFF.

---

![bg contain](https://help.figma.com/hc/article_attachments/24794089084695)

---

We want to make sure the ellipses are equally distributed both horizontally and vertically, as well as center-aligned to the frame. We can do this with Smart selection.

1. Hold Shift and click each ellipse to select all four at once.

2. Pink handles will appear when you hover over the selection, indicating a Smart selection has been created. 

3. Click and drag the pink handles to set the vertical and horizontal spacing between ellipses to 24.

4. Click and drag the selection to snap the ellipses to the center of the frame using the red alignment guides.

---

## Duplicate the frame and rotate the ellipses

Now, let’s create a second frame by duplicating the current frame.

1. Select the **loading/1** frame and use the duplicate shortcut to create a copy.

1. Rename the new frame to **loading/2**.

1. Select **loading/2**, and press **Enter** to select all nested layers. In this case, all four ellipses will be selected.

1. Hover your mouse near the object’s corner until the **rotate** icon appears.

1. Hold **Shift** on your keyboard, then click and drag clockwise to rotate the ellipse's positions by -90 degrees. You can check the rotation amount in the right sidebar using the **Angle** input field.

---

![bg contain](https://help.figma.com/hc/article_attachments/24799985202839)

---

## Duplicate the second frame and resize the ellipses

Let’s create the final frame that will tie it all together.


1. Duplicate the **loading/2** frame.

2. Rename the new frame to **loading/3**.

3. Select **loading/3**, and press **  ** to select all ellipses.

---

4. Update the size of the ellipses to **60 W** and **60 H** using the settings in the right sidebar.

5. Use the **Align horizontal** centers and the **Align vertical** centers settings in the alignment controls panel to center all four ellipses.

6. With all four ellipses still selected, drag to place them in the center of the frame.

---

![bg contain](https://help.figma.com/hc/article_attachments/24799998351639)

---

## Add prototype connections

Now that the setup is complete, we’ll add prototype connections to get our loading animation moving.


1. Click the **Prototype** tab on the right sidebar.

2. Select the **loading/1** frame, then hover over the edge of the frame until you see the blue plus sign.

3. Click and drag the connection to the **loading/2** frame. This opens the Interaction details modal.

---

4. From the dropdown menu, set the trigger to **After delay** and set the duration to 100ms.

5. Set the action to **Navigate to** and the destination to **loading/2**.

6. Set the prototype animation to **Smart animate**.

7. From the animation type dropdown menu, select **Custom bezier** and set the duration to 300ms.

8. In the Bézier curve input field, enter 0.5, -0.1, 0.5, 1.1.

---

![bg contain](https://help.figma.com/hc/article_attachments/24799998355095)

---

Nice! Now we can connect the remaining frames.

1. Click and drag a prototype connection from loading/2 to loading/3.

1. Set the trigger to After delay and duration to 100ms. Figma remembers the previous prototype animation settings, so you don’t have to set up the animation from scratch again.

1. Create a prototype connection from loading/3 back to loading/1 to make a looped animation.

1. Set the trigger to After delay and duration to 100ms.

Now it’s time to see our animation in action. Click the flow starting point button next loading/1 frame to open inline preview.

---

![bg contain](https://help.figma.com/hc/article_attachments/24800411588119)

---

Looks wonderful! With just a few frames, shapes, and prototype connections, we created a loading animation. If you’re interested in using this animation on multiple pages, keep reading to learn how to turn it into a reusable component set.

## Create a component set

The loading animation looks great! But having to recreate it every time you want to use it would be a pain. Luckily, we can create a component set so you can reuse the animation again and again.


1. Hold Shift on your keyboard and select all three frames.

2. From the toolbar, open the **Create component** dropdown menu.

3. Select **Create component set**.

---

![bg contain](https://help.figma.com/hc/article_attachments/24801617329687)

---

Because our frames were named **loading/1**, **loading/2**, and **loading/3**, they are automatically turned into a component set called “loading” with three variants called “1”, “2”, and “3”. If we weren’t consistent with our naming, the component set would simply be called “Component 1”.

Let’s remove the background fill on the variants so they can be used over other designs.

1. Hold Shift on your keyboard, and then click on each variant to select all three.

2. Click the minus button under **Fill** in the right sidebar.

---

## Add an instance to a new frame

Now that we have a component set, we can add an instance of it to a new frame.

1. Click the **Frame** icon from the toolbar, or press F.

1. From the Design tab in the right sidebar, select the **iPhone 14 Pro** preset size.

1. Update the fill to #1D1D1D.

1. Select the 1 variant.

1. Hold ⌥ Option (Mac) or Alt (Windows) and drag the variant to create an instance. Place the instance in the center of the frame.

1. Click the **Present** button in the toolbar to test it out.

---


![bg contain](https://help.figma.com/hc/article_attachments/24970044664727)

---

## What's next?

Congratulations! You’ve created a loading animation with just a few frames. If you’re looking for another challenge, try making some tweaks to the animation, adding other frames and colors like this one below.

---

![bg contain](https://help.figma.com/hc/article_attachments/24802509742999)

---

## Prototype scroll and overflow behavior

---

Set how scrolling and panning works in your prototypes to replicate user interactions, such as:

- Scroll up and down a long page of content
- Scroll left and right to view different elements in a slider
- Pan or scroll in any direction, like in an interactive map
- Fix objects like navigation bars and menus to one position on the page while scrolling
- Create “sticky objects” that stay in place at the top of the frame once you scroll past them

---

In order to use scrolling in your Figma prototypes, you must:

- Prepare frames for scrolling: Make sure content extends beyond the bounds of the frame’s dimensions.
- Apply scroll overflow to frame: Define if your frame will have vertical, horizontal, both, or no scrolling.
- Apply scroll position to the objects within frame: Define how objects in your frame behave when you scroll past them. - They can scroll with the parent frame, stay in a fixed position, or stick to the top of their parent frame.

Once you’ve set up scrolling, you can also consider preserving or resetting scroll position when navigating between multiple frames.

---

## Prepare frames for scrolling

In order to add scrolling behavior to a frame, the frame must have content that extends beyond the bounds of the frame.

Think of it like any webpage—when you browse on your phone, you can only see the content that fits the dimensions of your screen. However, there is “hidden” content that exists beyond what you see on your screen that you can only see with scrolling.

---

## Extend content beyond frame dimensions

To resize a frame:

- Select the frame you want to update.
- Open the Design panel in the right sidebar.
- Hover over the frame's edge until the cursor appears.
- Drag the bounding box to resize the frame.

To ensure that each object still sits within the selected frame, check the Layers section of the left navigation panel. Child objects are nested beneath their parent frame.

---

![bg contain](https://help.figma.com/hc/article_attachments/26978261589911)

---

## Clip content

You can hide any content that extends beyond the bounds of a frame with Clip content.

- Select the frame you want to update.
- Open the Design tab in the right properties panel.
- In the Layout section, check the box next to Clip content.

---

![bg contain](https://help.figma.com/hc/article_attachments/26978254304535)

---

## Apply scroll overflow to frames

Scroll overflow defines how users can interact with content that extends beyond a frame’s dimensions.

You can only apply overflow behavior to frames. This applies to frames that are directly on the canvas (top-level frames), as well as frames nested within other frames or layers.

---

To apply scroll overflow to a frame:

1. Select a frame.
2. Open the Prototype tab in the right properties panel.
3. In the Scroll behavior section, select the Overflow dropdown. Choose from:
- No scrolling
- Horizontal
- Vertical
- Both directions

---

![bg contain](https://help.figma.com/hc/article_attachments/26978261594263)

---

## Vertical

Vertical scrolling allows users to swipe or scroll up and down. Use this behavior to mimic scrolling down a long website, or page of content within an app.

![](https://help.figma.com/hc/article_attachments/13321748595991)

---

## Horizontal

Horizontal scrolling allows users to swipe or scroll left and right, while maintaining their vertical position. Use this to create sliders for content, like products, galleries, and libraries.

![](https://help.figma.com/hc/article_attachments/13321750794903)

---

## No scrolling

No scrolling prevents users from scrolling in any direction. Content that extends beyond the bounds of the frame will not be viewable.

---

## Both directions

Both directions (horizontal and vertical) lets users navigate in any direction, like when viewing a map or enlarged image.

![](https://help.figma.com/hc/article_attachments/19855785533335)

---

## Apply scroll position to objects within a frame

Scroll position defines how layers in a frame behave when users scroll past them. You can only apply one scroll position to each layer.

1. Select an object, group, or component. The object must be on a frame that has scroll overflow applied.
2. Open the Prototype tab in the right properties panel.
3. In the Scroll behavior section, select the Position dropdown. Choose from:
- Scroll with parent
- Fixed
- Sticky

---

![bg contain](https://help.figma.com/hc/article_attachments/26978254308247)

---

## Scroll with parent

Objects that scroll with parent move up and down the frame as you scroll. Use this behavior to mimic the behavior of scrolling up and down longer pages of content. 

![](https://help.figma.com/hc/article_attachments/13321952490647)

---

## Fixed

Fixed objects don’t move, even as you scroll up and down. For example, use this option to fix a status bar to the top of the device, or fix a menu to the bottom of a frame.

You cannot assign a fixed scroll position to any objects in a frame with auto layout, unless the object has absolute position applied.

![](https://help.figma.com/hc/article_attachments/13321956295447)

---

When you set an object to fixed, Figma will move it above the other layers in the frame and label them as Fixed in the Layers section of the left navigation panel. It's not possible to position scrolling objects above fixed layers.

![](https://help.figma.com/hc/article_attachments/26978261598871)

---

## Sticky

Apply sticky scroll position to any object within a frame that has vertical scrolling.

Sticky objects will scroll at first, but become fixed once its top edge reaches the top of its parent frame. (If you scroll up again, the object will unstick and move down the parent frame.)

![](https://help.figma.com/hc/article_attachments/13322051524119)

---

If the sticky object is nested within another layer in a frame, it stays within its direct parent’s bounds. This means that when the direct parent layer is scrolled out of view, the sticky object continues scrolling with its parent.

![](https://help.figma.com/hc/article_attachments/18926153090967)

---

Check the Layers section in the left navigation panel to see how sticky objects will stack when scrolling. Any layers below a sticky object will scroll behind it, and any layers above a sticky object will scroll in front of it. To change the order in which your objects stack for sticky scroll, change their order in the Layers panel.

---

## Preserve and reset scroll position

When your prototype contains multiple pages or screens, you can choose to preserve scroll position or reset scroll position between frames.

- Preserve scroll position: Maintain the user’s scroll position when they transition between frames
- Reset scroll position: Reset the user’s scroll position when they transition between frames
