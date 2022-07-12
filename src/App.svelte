<script>
  import logo from "./assets/svelte.png";
  import Book from "./lib/Book.svelte";
  import Cats from "./lib/Cats.svelte";
  import ClassBinding from "./lib/ClassBinding.svelte";
  import ContentEditable from "./lib/ContentEditable.svelte";
  import Counter from "./lib/Counter.svelte";
  import CounterWithStore from "./lib/CounterWithStore.svelte";
import DyinamicElements from "./lib/DyinamicElements.svelte";
import DynamicHeadElments from "./lib/DynamicHeadElments.svelte";
  import EmiteEvents from "./lib/EmiteEvents.svelte";
  import EventModifiers from "./lib/EventModifiers.svelte";
  import Form from "./lib/Form.svelte";
  import HarryPotterStudents from "./lib/HarryPotterStudents.svelte";
  import Input from "./lib/Input.svelte";
import LoadComponent from "./lib/LoadComponent.svelte";
  import Logged from "./lib/Logged.svelte";
  import MouseEvents from "./lib/MouseEvents.svelte";
  import PostSlot from "./lib/PostSlot.svelte";
  import TodoList from "./lib/TodoList.svelte";
  import User from "./lib/User.svelte";
  import UserAgeChecker from "./lib/UserAgeChecker.svelte";
  import WidgetSlot from "./lib/WidgetSlot.svelte";

  const alertText = () => {
    alert("Algún texto");
  };

  const book = {
    title: "Arpnede Svelete.js",
    author: "Rich Harris",
    isbn: "asdfasd4a45",
    published: true,
  };

  const handleMessageEvent = (e) => {
    alert(e.detail.text);
  };

  let inputField;
</script>

<main>
  <img src={logo} alt="Svelte Logo" />
  <h1>Hello world!</h1>

  <Counter />

  <hr />

  <User name="Jhon Fabio Cardona" on:click={alertText} />

  <hr />

  <Form />

  <hr />

  <Book {...book} />

  <hr />

  <Logged />

  <hr />

  <UserAgeChecker />

  <hr />

  <Cats />

  <hr />

  <HarryPotterStudents />

  <hr />

  <MouseEvents />

  <hr />

  <EventModifiers />

  <hr />

  <EmiteEvents on:message={handleMessageEvent} />

  <hr />

  <ContentEditable />

  <hr />

  <TodoList />

  <hr />

  <Input bind:this={inputField} />
  <button
    on:click={() => {
      inputField.focus();
    }}>Aplicar focus al input</button
  >

  <hr />
  <CounterWithStore />

  <hr />
  <ClassBinding />

  <hr />
  <PostSlot>
    <h2>Contenido del Post</h2>
  </PostSlot>

  <hr />
  <WidgetSlot>
    <span slot="title">
      Título del Widget
    </span>
   
    <span slot="content">
      Contenido del Widget
    </span>

    <span slot="footer">
      Footer del Widget
    </span>
  </WidgetSlot>

  <hr>
  <LoadComponent/>

  <hr>
  <DyinamicElements/>

  <hr>
  <DynamicHeadElments/>

  <p />

  <!-- <p>
    Visit <a href="https://svelte.dev">svelte.dev</a> to learn how to build Svelte
    apps.
  </p>

  <p>
    Check out <a href="https://github.com/sveltejs/kit#readme">SvelteKit</a> for
    the officially supported framework, also powered by Vite!
  </p> -->
</main>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  }

  main {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
  }

  img {
    height: 16rem;
    width: 16rem;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4rem;
    font-weight: 100;
    line-height: 1.1;
    margin: 2rem auto;
    max-width: 14rem;
  }

  p {
    max-width: 14rem;
    margin: 1rem auto;
    line-height: 1.35;
  }

  @media (min-width: 480px) {
    h1 {
      max-width: none;
    }

    p {
      max-width: none;
    }
  }
</style>
