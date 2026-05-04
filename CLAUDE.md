# Enetra Prototype

## Rules
- Do not modify existing files unless explicitly asked.
- Do not work in `components/` unless explicitly asked.
- No breadcrumbs on any page.
- For styling gaps not covered here, choose the closest matching style from the patterns below.

## Page shell
Every page shares the same header, footer, and main content wrapper. No exceptions.
Exception: auth pages (login, register, forgot-password, reset-password) use the auth shell below instead.

```html
<body class="bg-slate-50 font-[Inter,sans-serif] text-slate-800 min-h-screen flex flex-col">
<header class="select-none bg-white border-b border-slate-200 flex h-14 items-center justify-between px-6 shrink-0">
<main class="px-6 lg:px-12 py-12 flex-1">
  <div class="max-w-[1344px] mx-auto w-full flex flex-col gap-8">
<footer class="select-none bg-white border-t border-slate-200 flex items-center justify-between px-6 h-12">
```

## Auth shell
No header or footer. Logo centered above a `max-w-sm` card. Use for all auth-related pages.

```html
<body class="bg-slate-50 font-[Inter,sans-serif] text-slate-800 min-h-screen flex flex-col items-center justify-center px-4 py-12">
  <div class="w-full max-w-sm flex flex-col items-center gap-8">
    <img src="/images/enetra-logo.png" alt="Enetra" class="h-6 object-contain" />
    <div class="w-full p-8 bg-white rounded-lg shadow-[0px_1px_4px_0px_rgba(0,0,0,0.10)] outline outline-1 outline-offset-[-1px] outline-slate-200 flex flex-col gap-6">
```

Form inputs: `h-10 bg-white px-4 rounded-[3px] outline outline-1 outline-offset-[-1px] outline-slate-400 flex items-center`
Input label: `text-sm font-semibold text-slate-800`
Full-width submit button: same primary button style with `w-full py-2.5 justify-center`.
Password show/hide: two `<i>` tags with `x-show`, never `:data-lucide` (Lucide initialises once).
Success states: `x-data="{ sent/saved: false }"` on the card, `<template x-if>` to swap content.

## Colors
- Text primary: `text-slate-800`
- Text secondary/meta: `text-slate-500`
- Interactive / links: `text-cyan-700`
- Primary action bg: `bg-cyan-700 hover:bg-cyan-800`
- Page bg: `bg-slate-50`, surface bg: `bg-white`

## Cards
White: `p-6 bg-white rounded-lg shadow-[0px_1px_4px_0px_rgba(0,0,0,0.10)] outline outline-1 outline-offset-[-1px] outline-slate-200`
Cyan (highlighted): `p-6 bg-cyan-50 rounded-lg shadow-[0px_1px_4px_0px_rgba(21,94,117,0.10)] outline outline-1 outline-offset-[-1px] outline-cyan-200`
Card header divider: `pb-4 border-b border-slate-200`
Card title: `text-xl font-bold text-cyan-700 hover:underline`
Card grids use `grid grid-cols-3 gap-4` (or `gap-5`).

## Buttons
Primary (solid): `select-none px-6 py-2 bg-cyan-700 hover:bg-cyan-800 transition-colors duration-150 rounded-full flex items-center gap-2 cursor-pointer` — white icon + label inside.
Secondary (outlined): `select-none px-6 py-2 text-cyan-700 rounded-full outline outline-1 outline-offset-[-1px] outline-cyan-700 hover:bg-cyan-700 hover:text-white transition-colors duration-150 flex justify-center items-center gap-3 cursor-pointer`
All interactive elements use `transition-colors duration-150`.

## Toolbar section
Starts with `border-t-2 border-slate-200 pt-8`. Single flex row: search → sort dropdown → card/table view toggle → primary button (`ml-auto`). Wrapping div owns `x-data="{ view: 'card' }"`.

## Dropdowns
`x-data="{ open: false }"` on wrapper, `@click.outside="open = false"`, panel: `absolute bg-white rounded-[4px] shadow-[0px_4px_6px_rgba(0,0,0,0.15)] outline outline-1 outline-offset-[-1px] outline-slate-200 z-10`. Table container: no `overflow-hidden` (breaks dropdowns).

## Status badges
`px-3 py-0.5 rounded-full text-xs font-semibold`
- Green (Berechnet): `bg-green-100 text-green-800`
- Amber (In Bearbeitung): `bg-amber-100 text-amber-800`
- Cyan (Basis): `bg-cyan-200 text-cyan-800`

## Tables
Container: `rounded-lg shadow-[0px_1px_4px_0px_rgba(0,0,0,0.10)] outline outline-1 outline-offset-[-1px] outline-slate-200` (no `overflow-hidden`).
`thead` cells: `px-6 py-3 text-xs font-semibold text-slate-500 uppercase tracking-wider`
`tbody` rows: `hover:bg-slate-50 transition-colors duration-100`, cells: `px-6 py-4`
