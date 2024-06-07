# nextJsNotes | Stephen Grider
1. Rootlayout component is the parent root, most wrapping component in our app.
2. Tha layout file(layout.tsx responsible) in our app, the different pages when redered appear as children of the layout component. So a route called blogs having blog component will be a child of Layout component
3. Project Corp:
   - Built in image component used to render image and can resize image automatically based on the screen size and also cache the size for next time. Fill prpp in           Image component expand to fill up the parent element while laoading the image. Kinda like placeholder for loading image. HeroComponent, in traditional web-            developing, it is whats called for components with big image in background.
4. Project Snippet:
   - Server action is the no: 1 way to change data in next app. It is close integration with html forms. They are called with values user enter to form. Inorder for next to know its a server action fn, within the function we need to write string 'use server';
   - By default all components in next are server components, unlike the native client component in react. Better performance, UX etc. We can use async/await directly on the fn component and dont need useState or useEffect. In fact, using hooks in server component will throw error. Also, event handlers are not available as well. You can still use hooks and event handlers while defining client component('use client') and use that as a child component to make it dynamic. Even though client component executes on the browser and server component on the server, client component still gets rendered 1 time on the server-side and send it down to the browser. A little bit later on, its js is also sent down.
   - When rendering data, if data not found, we can define a not-found.tsx file and render it. You can define the file anywhere but Next will look for the closest not-found file within the folder structure and use that. If no file defined, next will use its default one.
   - After the development, during prod build, next will decide which all pages are dynamic and static and it does something called Full-Route cache. So, some page, like home, if it requires data render dynamically, new data will not be loaded because next might have configured it as static page and render the one time static page of the home page with the cached data. After runnign build command, routes with O sign are static while lambda sign are dynamic. We can use many methods in next to change the static page into dynamic. We can also manipulate to purge or update the cache. There are other type of cache also(Data cache, Router Cache) and caching are important for performance. revalidatePath fn called before redirect is one possible solution
   - Also in prod mode, for dynamic pages, we can cache datas that are already in the db using generateStaticParams fn. Next will cache all the data with its id and use it while loading show page of data.
5. Project Discuss:
   - Use Pathhelpers to define all the paths, so that if a parent path changes, you dont have to change all the path instead just the variable where path helper defined. Used for large/medium projects.
   - For home pages, time based cache of static data is better, we dont need to show user new post exactly when it was created, saving performance. Just preferences.
