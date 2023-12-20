# ai.nvim

A Neovim plugin powered by Google Gemini.

## Installation

First [get an API key](https://ai.google.dev/tutorials/setup) from Gemini. It's free!

Using lazy.nvim:

```lua
{
  'firemariovn/ai.nvim',
  dependencies = 'nvim-lua/plenary.nvim',
  opts = {
    api_key = 'YOUR_GEMINI_API_KEY', -- or read from env: `os.getenv('GEMINI_API_KEY')`
    -- The locale for the content to be defined/translated into
    locale = 'en',
    -- The locale for the content in the locale above to be translated into
    alternate_locale = 'vn',
  },
  cmd = { 'GeminiDefine', 'GeminiDefineV', 'GeminiTranslate', 'GeminiAsk' },
},
```

## Usage

### Define a word or phrase

```viml
" Define the word under cursor
:GeminiDefine

" Define the specified word
:GeminiDefine happy
```

Define the selected word or phrase:

```viml
:'<,'>GeminiDefineV
```

### Translate contents

```viml
" Translate selection
:GeminiTranslate

" Translate the specified content
:GeminiTranslate I am happy.
```

### Ask anything

```viml
" Use selection as the prompt
:GeminiAsk

" Pass prompt explicitly
:GeminiAsk How to add two numbers in TypeScript?
```

## Credit

Forked from [ai.nvim](https://github.com/gera2ld/ai.nvim) from gera2ld. Thank you!
