# Event Schedule Pages

This repository contains two versions of an interactive event schedule webpage built with Chart.js.

## Files

### event-schedule.html
**The Original Version** - A clean, streamlined implementation perfect for:
- Quick prototyping and demos
- Internal tools and dashboards
- Projects where accessibility is not a primary requirement
- Learning how Chart.js works with event timelines

**Features:**
- Interactive Chart.js timeline visualization
- Click to view event details
- Multi-day schedule support
- Dark mode support
- Responsive design
- ~770 lines of code

### event-schedule-v2.html
**The Accessible Version** - Full WCAG 2.2 AA compliance for:
- Public-facing websites
- Government and educational institutions
- Enterprise applications with accessibility requirements
- Products requiring Section 508 or ADA compliance
- International markets with accessibility regulations

**Features:**
- Everything from v1, plus:
- Full keyboard navigation (arrow keys, Enter, Escape)
- Complete screen reader support with ARIA labels
- Focus management and visible focus indicators
- Skip links and semantic HTML
- High contrast color ratios (WCAG AA compliant)
- Hidden text-based schedule alternative
- Dialog focus trap and proper modal behavior
- ~1,200 lines of code

## Quick Comparison

| Feature | v1 (Basic) | v2 (Accessible) |
|---------|------------|-----------------|
| Click to view events | ✅ | ✅ |
| Multi-day support | ✅ | ✅ |
| Dark mode | ✅ | ✅ |
| Responsive design | ✅ | ✅ |
| Keyboard navigation | ❌ | ✅ Full |
| Screen reader support | ⚠️ Basic | ✅ Complete |
| ARIA labels/roles | ❌ | ✅ |
| Focus indicators | ⚠️ Browser default | ✅ Custom 3px |
| Color contrast (WCAG AA) | ⚠️ Partial | ✅ Full |
| Skip links | ❌ | ✅ |
| Focus management | ❌ | ✅ |
| Accessible alternative | ❌ | ✅ Hidden text schedule |
| WCAG 2.2 AA Compliant | ❌ | ✅ |

## How to Choose

### Use v1 if:
- Building a quick prototype or proof of concept
- Creating an internal tool for your team
- Accessibility is not a requirement
- You need a simpler codebase to learn from
- File size/complexity matters more than compliance

### Use v2 if:
- Building a public-facing website
- Your organization requires accessibility compliance
- You need to meet WCAG 2.2 AA standards
- Supporting users with disabilities is important
- You're in a regulated industry (government, education, healthcare)
- You want best-practice accessibility patterns

## Customization

Both files use the same configuration format. Edit the `TYPES` object and `DAYS` array at the top of the `<script>` section:

```javascript
const TYPES = {
  keynote: 'Keynote',
  talk: 'Session',
  workshop: 'Workshop',
  break: 'Break',
  meal: 'Meal',
  social: 'Social'
};

const DAYS = [
  {
    name: 'Day 1',
    sub: 'Monday, Oct 16',
    items: [
      ['Event Name', 9, 10, 'talk', 'Room A', 'Description', [['Link', 'url']]]
      // [name, startTime, endTime, type, location, description, links]
    ]
  }
];
```

## Documentation

- **ACCESSIBILITY.md** - Complete WCAG 2.2 compliance documentation for v2
  - Detailed accessibility features breakdown
  - Testing procedures and tools
  - Keyboard shortcuts reference
  - Screen reader testing guide
  - Color contrast specifications

## Dependencies

Both versions require:
- Chart.js 4.4.1 (loaded from CDN)
- Modern browser with ES6 support

## Browser Support

Both versions tested and working in:
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## License

Same as parent repository.

## Contributing

When contributing improvements:
- Bug fixes should be applied to both v1 and v2
- Accessibility improvements should be added to v2
- New features should consider both versions
- Maintain the simpler v1 for learning/prototyping use cases
