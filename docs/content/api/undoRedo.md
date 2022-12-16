---
title: UndoRedo
metaTitle: UndoRedo - JavaScript Data Grid | Handsontable
permalink: /api/undo-redo
canonicalUrl: /api/undo-redo
searchCategory: API Reference
hotPlugin: true
editLink: false
description: Use the UndoRedo plugin with its API options and methods to revert and restore your changes.
react:
  metaTitle: UndoRedo - React Data Grid | Handsontable
---

# UndoRedo

[[toc]]

## Description

Handsontable UndoRedo plugin allows to undo and redo certain actions done in the table.

__Note__, that not all actions are currently undo-able. The UndoRedo plugin is enabled by default.

**Example**  
```js
undo: true
```

## Options

### undo
  
::: source-code-link https://github.com/handsontable/handsontable/blob/155272763a14b785c449c1c1d175c594050fe92d/handsontable/src/dataMap/metaManager/metaSchema.js#L4523

:::

_undoRedo.undo : boolean_

The `undo` option configures the [`UndoRedo`](@/api/undoRedo.md) plugin.

You can set the `undo` option to one of the following:

| Setting | Description                                        |
| ------- | -------------------------------------------------- |
| `true`  | Enable the [`UndoRedo`](@/api/undoRedo.md) plugin  |
| `false` | Disable the [`UndoRedo`](@/api/undoRedo.md) plugin |

By default, the `undo` option is set to `undefined`,
but the [`UndoRedo`](@/api/undoRedo.md) plugin acts as enabled.
To disable the [`UndoRedo`](@/api/undoRedo.md) plugin completely,
set the `undo` option to `false`.

Read more:
- [Undo and redo](@/guides/accessories-and-menus/undo-redo.md)

**Default**: <code>undefined</code>  
**Example**  
```js
// enable the `UndoRedo` plugin
undo: true,
```

## Methods

### clear
  
::: source-code-link https://github.com/handsontable/handsontable/blob/155272763a14b785c449c1c1d175c594050fe92d/handsontable/src/plugins/undoRedo/undoRedo.js#L334

:::

_undoRedo.clear()_

Clears undo history.



### destroy
  
::: source-code-link https://github.com/handsontable/handsontable/blob/155272763a14b785c449c1c1d175c594050fe92d/handsontable/src/plugins/undoRedo/undoRedo.js#L396

:::

_undoRedo.destroy()_

Destroys the instance.



### disable
  
::: source-code-link https://github.com/handsontable/handsontable/blob/155272763a14b785c449c1c1d175c594050fe92d/handsontable/src/plugins/undoRedo/undoRedo.js#L376

:::

_undoRedo.disable()_

Disables the plugin.



### done
  
::: source-code-link https://github.com/handsontable/handsontable/blob/155272763a14b785c449c1c1d175c594050fe92d/handsontable/src/plugins/undoRedo/undoRedo.js#L175

:::

_undoRedo.done(wrappedAction, [source])_

Stash information about performed actions.

**Emits**: [`Hooks#event:beforeUndoStackChange`](@/api/hooks.md#beforeundostackchange), [`Hooks#event:afterUndoStackChange`](@/api/hooks.md#afterundostackchange), [`Hooks#event:beforeRedoStackChange`](@/api/hooks.md#beforeredostackchange), [`Hooks#event:afterRedoStackChange`](@/api/hooks.md#afterredostackchange)  

| Param | Type | Description |
| --- | --- | --- |
| wrappedAction | `function` | The action descriptor wrapped in a closure. |
| [source] | `string` | `optional` Source of the action. It is defined just for more general actions (not related to plugins). |



### enable
  
::: source-code-link https://github.com/handsontable/handsontable/blob/155272763a14b785c449c1c1d175c594050fe92d/handsontable/src/plugins/undoRedo/undoRedo.js#L356

:::

_undoRedo.enable()_

Enables the plugin.



### isEnabled
  
::: source-code-link https://github.com/handsontable/handsontable/blob/155272763a14b785c449c1c1d175c594050fe92d/handsontable/src/plugins/undoRedo/undoRedo.js#L345

:::

_undoRedo.isEnabled() ⇒ boolean_

Checks if the plugin is enabled.



### isRedoAvailable
  
::: source-code-link https://github.com/handsontable/handsontable/blob/155272763a14b785c449c1c1d175c594050fe92d/handsontable/src/plugins/undoRedo/undoRedo.js#L323

:::

_undoRedo.isRedoAvailable() ⇒ boolean_

Checks if redo action is available.


**Returns**: `boolean` - Return `true` if redo can be performed, `false` otherwise.  

### isUndoAvailable
  
::: source-code-link https://github.com/handsontable/handsontable/blob/155272763a14b785c449c1c1d175c594050fe92d/handsontable/src/plugins/undoRedo/undoRedo.js#L312

:::

_undoRedo.isUndoAvailable() ⇒ boolean_

Checks if undo action is available.


**Returns**: `boolean` - Return `true` if undo can be performed, `false` otherwise.  

### redo
  
::: source-code-link https://github.com/handsontable/handsontable/blob/155272763a14b785c449c1c1d175c594050fe92d/handsontable/src/plugins/undoRedo/undoRedo.js#L265

:::

_undoRedo.redo()_

Redo the previous action performed to the table (used to reverse an undo).

**Emits**: [`Hooks#event:beforeUndoStackChange`](@/api/hooks.md#beforeundostackchange), [`Hooks#event:afterUndoStackChange`](@/api/hooks.md#afterundostackchange), [`Hooks#event:beforeRedoStackChange`](@/api/hooks.md#beforeredostackchange), [`Hooks#event:afterRedoStackChange`](@/api/hooks.md#afterredostackchange), [`Hooks#event:beforeRedo`](@/api/hooks.md#beforeredo), [`Hooks#event:afterRedo`](@/api/hooks.md#afterredo)  


### undo
  
::: source-code-link https://github.com/handsontable/handsontable/blob/155272763a14b785c449c1c1d175c594050fe92d/handsontable/src/plugins/undoRedo/undoRedo.js#L218

:::

_undoRedo.undo()_

Undo the last action performed to the table.

**Emits**: [`Hooks#event:beforeUndoStackChange`](@/api/hooks.md#beforeundostackchange), [`Hooks#event:afterUndoStackChange`](@/api/hooks.md#afterundostackchange), [`Hooks#event:beforeRedoStackChange`](@/api/hooks.md#beforeredostackchange), [`Hooks#event:afterRedoStackChange`](@/api/hooks.md#afterredostackchange), [`Hooks#event:beforeUndo`](@/api/hooks.md#beforeundo), [`Hooks#event:afterUndo`](@/api/hooks.md#afterundo)  
