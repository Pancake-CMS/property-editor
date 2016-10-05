# property-editor
A web component that provides an editor for a property based on its type.

## Installation

```shell
bower install --save pancake-cms-property-editor
```

## Attributes

| name | type | description |
|------|------|-------------|
| data | Object | The property object obtained from a component |

### Examples of `data` object

These are the examples for various scenarios

#### For single line input

```javascript
{
    name: 'gridColumnStart',
    value: 1,
    type: 'text',
    description: 'The start column location of this component'
};
```

#### For multi line input

```javascript
{
    name: 'randomErrorMessage',
    value: 'this update statement has a logic bug how can you update the user with id 6 \n and tell the update to make the id 1, the uid is unique (primary key) for the user table and you must remove the ( uid = \'1\' ) from this statement, \nor report a bug if this is from a Contributed module',
    type: 'textarea',
    description: 'The statement is copied from https://www.drupal.org/node/933472'
};
```

#### For checkbox selection

```javascript
{
    name: 'isDialogBoxOpen',
    value: true,
    type: 'checkbox',
    description: 'Open the dialog box by default'
};
```

and

```javascript
{
    name: 'shouldOpenLinkInNewTab',
    value: false,
    type: 'checkbox',
    description: 'Should this link be opened in a new tab?'
};
```

#### For radio buttons

```javascript
{
    name: 'subscribe',
    value: 'yes',
    type: 'radio',
    options: [
            'yes',
            'no',
        ],
    description: 'Unsubscribe option'
};
```

#### For dropdowns

```javascript
{
    name: 'selectedProduct',
    value: '1',
    type: 'dropdown',
    options: [
            'Windows',
            'MacBook',
            'Linux'
        ],
    description: 'Which Product should be shown by default'
};
```

## Events

The `property-editor` triggers a `property-changed` event which provides the following data in its `detail` object

```javascript
{
    name : 'The name of the property',
    value: 'The new value'
}
```