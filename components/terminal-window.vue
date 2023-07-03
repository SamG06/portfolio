<template>
  <div id="siteTerminal" class="terminal">
    <div class="terminal-window-top">
      Terminal Navigation
    </div>
    <div class="window-top-separator" />
    <p id="loggedIn" />
    <p id="goto" />
    <p id="github" />
    <div id="previousCommands" />
    <div class="terminal-input-container">
      <label id="terminalLabel" for="terminalInput" />
      <div class="caret-container">
        <div id="caret" class="caret" />
        <input id="terminalInput" class="terminal-typing" type="text" spellcheck="false">
      </div>
    </div>
  </div>
</template>
<script setup>

</script>

<style scoped>
/* TERMINAL STYLES */
.terminal > * {
  font-family: "Fira Code";
  color: var(--light-purple);
}

.terminal {
  background: #3f2446;
  width: 90%;
  max-width: 500px;
  height: 350px;
  padding: 13px;
  position: relative;
  left: 0;
  border-radius: 3px;
  overflow: hidden;
  font-size: 14px;
  min-height: 250px;
  border: 1px solid #551d63;
  background-image: url("data:image/svg+xml,%3Csvg width='12' height='16' viewBox='0 0 12 16' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M4 .99C4 .445 4.444 0 5 0c.552 0 1 .45 1 .99v4.02C6 5.555 5.556 6 5 6c-.552 0-1-.45-1-.99V.99zm6 8c0-.546.444-.99 1-.99.552 0 1 .45 1 .99v4.02c0 .546-.444.99-1 .99-.552 0-1-.45-1-.99V8.99z' fill='%23413259' fill-opacity='0.22' fill-rule='evenodd'/%3E%3C/svg%3E");
}

.terminal-window-top {
  background: #371c3e;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  padding: 10px;
  color: #bfbfbf;
  font-size: 14px;
  font-weight: 300;
}

.window-top-separator {
  margin-top: 15px;
}

.projects-container {
  display: flex;
  flex-flow: column;
  align-items: center;
}
.terminal-input-container {
  display: flex;
}

.terminal-input-container label {
  width: 135px;
  flex-grow: 1;
  min-width: 105px;
}

input.terminal-typing {
  background: none;
  border: none;
  outline: none;
  width: 100%;
  color: rgb(87, 197, 87);
  font-size: 14px;
  font-weight: 600;
  caret-color: transparent;
}

.caret-container {
  position: relative;
  width: 100%;
}

.caret {
  background: var(--light-purple);
  width: 6px;
  height: 15px;
  position: absolute;
  left: 0;
  bottom: 2px;
  opacity: 0;
}
</style>
