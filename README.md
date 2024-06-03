# nextJsNotes | Stephen Grider
1. Rootlayout component is the parent root, most wrapping component in our app.
2. Tha layout file(layout.tsx responsible) in our app, the different pages when redered appear as children of the layout component. So a route called blogs having blog component will be a child of Layout component
3. Project Corp:
  a. Built in image component used to render image and can resize image automatically based on the screen size and also cache the size for next time. Fill prpp in           Image component expand to fill up the parent element while laoading the image. Kinda like placeholder for loading image. HeroComponent, in traditional web-            developing, it is whats called for components with big image in background.
5. Project Snippet:
  a. Server action is the no: 1 way to change data in next app. It is close integration with html forms. They are called with values user enter to form. Inorder for next to know its a server action fn, within the function we need to write string 'use server';
