# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components. Explain why each piece might be its own component.

    ```md
  You could have a list component, and each item on the list might be its own
  component because each item would likely employ the same behaviors. For example,
  each item could be crossed out or removed. It is this sort of repetitious behavior
  across all list items that makes them components.
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember generate component my-map
    ```

1.  What files are created and/or edited to produce a component, and what are their responsibilities?

    ```md
    component.js and template.hbs. component.js is where you define the behaviors
    that can be used on the component (example, crossing an item off a list, removing an
    item from a list, etc.). template.hbs renders said behaviors.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` route. What is
    the syntax (code that is written) to render this component inside that template?

    ```html
    <span class="contact">{{contacts.my-contact}}</span>
    ```

1.  Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    <ul>
    {{#each my-contact.my-phone as |my-phone|}}
      {{contacts/my-phone my-phone=my-phone}}
    {{/each}}
    </ul>
    ```
