<template>
  <div flex items-center justify-between p2>
    <div flex="~ gap4">
      <h1 text-lg font-bold>AST Explorer</h1>
      <LanguageSelect />
      <ParserSelect />
      <ParserOptions v-if="currentParser.options.configurable" />
    </div>

    <div flex="~ gap-3">
      <span font-mono text-gray>{{ currentParser.version }}</span>
      <button @click="toggleDark">
        <div i-ri:sun-line dark:i-ri:moon-line />
      </button>
      <a
        href="https://github.com/sxzz/ast-explorer"
        target="_blank"
        flex
        items-center
      >
        <div i-ri:github-line />
      </a>
    </div>
  </div>
</template>
