# Chip Component Documentation

## Overview
The Chip component is a versatile UI element used to categorize, filter, or tag content. It supports multiple visual styles and configurations to fit various design needs.

## Variants & Styles
The Chip component has the following variations:

### **Shape Variants**
- **Rounded:** Used for fitler interactions
- **Squared:** Used for tagging content

### **Color Themes**
- **Light Colors:** 19 predefined light colors.
- **Dark Colors:** 19 predefined strong/dark colors.

### **Outlined Styles**
- **Outlined:** Used for filter hover states
- **Minimal:** Used for status tagging

### **Sizes**
- **Small:** Compact and suitable for dense interfaces.
- **Default:** Balanced size for general use.
- **Large:** Larger for emphasis or touch-friendly interactions.
- **Minimal:** Most compact size, can be used to indicate a status change.

## Properties
The Chip component supports the following properties:
- **Icon:** A customizable swappable instance that can represent different icons.
- **Avatar:** An optional avatar image that is off by default.
- **Label:** The main textual content of the Chip.
- **Delete Icon:** A customizable swappable instance; defaults to a close button.

![image](img/chips-anatomy.png)

In code this would look like:

``` ts
<Chip
    icon={<BellIcon />} 
    label="Notifications"
    deleteIcon={<DeleteIcon />}
    onDelete={handleDelete}
    size="large"
    variant="default"
/>

<Chip
    avatar={<Avatar alt="Leslie Knope" src="../path/to/leslie-knope.jpg" />}
    label="Leslie Knope"
    deleteIcon={<DeleteIcon />}
    onDelete={handleDelete}
    size="large"
    variant="default"
/>
```

### Usage Example
![image](img/chips-example-usage.png)

## Usage Guidelines
### When to Use
- Use Chips to categorize, filter, or tag content.
- Suitable for adding inline interactive elements.
- Can be used for user selections, such as filtering options in search interfaces.

### When Not to Use
- Avoid using Chips for primary actions (use buttons instead).
- Do not use Chips for long text; keep labels concise.

### Best Practices
- **Ensure readability:** Use the color variant options in the componant.
- **Use consistent spacing:** Maintain uniform padding between Chips.
- **Avoid overuse:** Too many Chips on a screen can cause clutter.
- **Pair with icons when needed:** Icons enhance clarity.

## Examples
### **Tagging System** (Squared)
For tagging content

![image](img/Tagging.png)

### **Filter Options** (Rounded)
#### For filter interactions use rounded variants in these states:
- **For Selected states use a Strong color** 
- **For Hover states use the Outlined variant**
- **Use default gray for usage in components**

![image](img/Filtering.png)

### Accessibility Considerations
- **All 38 color variants have been checked for accessibility.**
- **Provide focus indicators for keyboard navigation.**
- **Use aria-labels when necessary for screen readers.**