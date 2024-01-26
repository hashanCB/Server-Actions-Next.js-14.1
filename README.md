# Server-Actions-Next.js-14.1

# Client.js

      "use client";
      import { createPost } from "./Server.js";
      
      const MyClientComponent = () => {
        return (
          <form action={createPost}>
            <input type="text" name="name" />
            <input type="email" name="email" />
            <input type="password" name="password" />
      
            <button type="submit">Create Post</button>
          </form>
        );
      };
      
      export default MyClientComponent;


# Server.js


      "use server";
      
      export async function createPost(formData) {
        const name = formData.get("name");
        const email = formData.get("email");
        const password = formData.get("password");
      
       
      
        console.log({ name, email, password });
        return <div></div>;
      }
