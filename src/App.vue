<template>
  <div id="app">
    <div id="nav">
      <router-link to="/leads">
        <img class="navLogo" alt="EloGroup logo minimized" src="@/assets/logo_minimized.png">
      </router-link>
    </div>
    <div class="appContainer">
      <router-view/>
    </div>
  </div>
</template>

<script>
export default {
  name: "app",
  data: () => {
    return {
      loginButtonInner: "Entrar"
    }
  }
}
</script>

<style>
:root {
  --mainColor: rgb(39, 39, 39);
  --containersBackground: white;
  --darkerContrastColor: rgb(187, 187, 187); 

  --errorColor: red;

  --transitionTime: .15s;

  --tableHeaderBackgorund: rgb(158, 158, 158);
  --tableHeaderColor: var(--containersBackground);
  --tableRowColorBackground: var(--containersBackground);
  --tableRowColor: var(--mainColor);
  --tableEvenBackground: rgb(230, 230, 230);

  --scrollBarWidth: 10px;
}

* {
  margin: 0;
  outline: none;
  color: var(--mainColor);
}

html {
    overflow-y: overlay;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

#nav { 
  position: relative; 
  top: 0;
  display: flex;
  justify-content: space-between;
  flex-wrap: nowrap;
  align-items: center;
  background: var(--mainColor);
}
  
.navLogo {
  margin: 10px;
  height: 50px; 
}

.loginBtn {
  margin-right: 20px;
}

.appContainer {
  background: var(--containersBackground);

  position: absolute;
  left: 50%;
  top: 100px;
  transform: translateX(-50%);

  border: solid 1px var(--mainColor);
  padding: 15px;
}

/* Firefox */
* {
  scrollbar-width: auto;
  scrollbar-color: var(--mainColor) transparent;
}

/* Chrome, Edge, and Safari */
*::-webkit-scrollbar {
  width: var(--scrollBarWidth);
  height: var(--scrollBarWidth);
}

*::-webkit-scrollbar-track {
  background: transparent;
}

*::-webkit-scrollbar-thumb {
  background-color: var(--mainColor);
  border-radius: 10px;
  border: 1px solid var(--containersBackground);
}
</style>
