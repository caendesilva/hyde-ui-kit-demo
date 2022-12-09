# Hyde UI Kit - Documentation

The HydePHP UI Kit is a collection of minimalistic and un-opinionated TailwindCSS components for Laravel Blade,
indented to be used with HydePHP. Note that these components may require CSS classes not present in the bundled app.css
file and that you may need to recompile the CSS file using the included Laravel Mix configuration.

## Warning

The HydePHP UI Kit is still in development and is not yet ready for production use.
All components including their names can and probably will be changed.

## Components

### Buttons

<div style="display: flex;">
<img src="https://user-images.githubusercontent.com/95144705/206711385-66701bbf-1d86-4a6c-9625-fd7ea90d3805.png" alt="buttons-light" width="49.5%">
<img src="https://user-images.githubusercontent.com/95144705/206711382-56fd9dde-137a-49cc-87b8-53dcc1c15bc2.png" alt="buttons-dark" width="49.5%">
</div>

#### Primary

```blade
<x-hyde::ui.components.button-primary>
    Primary Button
</x-hyde::ui.components.button-primary>
```

#### Secondary

```blade
<x-hyde::ui.components.button-secondary>
    Secondary Button
</x-hyde::ui.components.button-secondary>
```

### Input

The base component is `<x-hyde::ui.components.input />`, any additional attributes will be passed to the input element as seen below.

```blade
<x-hyde::ui.components.input
    type="text"
    name="name"
    placeholder="Name"
    value="John Doe"
/>
```

### Card

An incredibly versatile component that can be used for a wide variety of purposes.

In the most basic form, a card is just a container with a white background and a shadow.
However, it also supports two slots: `title` and `footer`.

```blade
<x-hyde::ui.components.card>
    A card with some content.
</x-hyde::ui.components.card>
```

```blade
<x-hyde::ui.components.card>
    <x-slot name="title">
        Card Title
    </x-slot>
</x-hyde::ui.components.card>
```

```blade
<x-hyde::ui.components.card>
    <x-slot name="footer">
       Some footer content.
    </x-slot>
</x-hyde::ui.components.card>
```

Why not combine the components?

```blade
<x-hyde::ui.components.card>
    <x-slot name="title">
        My Amazing Card
    </x-slot>

    A card with some content and a footer with a button.

    <x-slot name="footer" class="text-center">
        <x-hyde::ui.components.button-primary>
            Primary Button
        </x-hyde::ui.components.button-primary>
    </x-slot>
</x-hyde::ui.components.card>
```
