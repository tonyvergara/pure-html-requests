# Form Builder V2 - Build Brief

**Date:** September 7, 2026  
**Based on:** FORM_BUILDER_UX_AUDIT.md recommendations  
**Target File:** sample-form-v2.html (new file, preserves original)

---

## Objectives

Rebuild the USWDS Form Builder to align with UX.md principles, focusing on:
- **Efficient yet supportive** user experience
- **Plain, direct language** (no jargon)
- **Warm, friendly** tone without being gimmicky
- **Clarity over cleverness**
- **WCAG AA accessibility** compliance

---

## Scope: Phase 1 Implementation

### ✅ CRITICAL FIXES (Must Do)

#### 1. Voice & Tone Overhaul
- Remove ALL technical jargon
- Rewrite ALL error messages to be supportive, not blaming
- Replace bureaucratic language with conversational, friendly copy
- Maintain professional tone (government-appropriate)

#### 2. Interface Labels
Replace developer-centric terms with user-focused language:
- "Form Architecture" → "Form Outline"
- "PAGES & SEQUENCING" → "Pages"
- "Component Label Typography Text" → "Label"
- "USWDS Instructional Hint Copy" → "Help text"
- "Contextual Error Assertion Message" → "Error message"
- "Mandatory Validation Constraint" → "Required"
- "Options Parameters (Comma-Separated Grid)" → "Options (comma-separated)"

#### 3. Default Form Content
Create realistic, user-friendly example form:
- Replace jargon-filled labels with clear, conversational text
- Use realistic scenarios (actual benefits application language)
- Demonstrate best practices for hint text and error messages
- Show proper progressive disclosure

#### 4. Error Messages - Complete Rewrite
All error messages must:
- Say what to do, not what went wrong
- Be specific and actionable
- Never blame the user
- Use plain language

#### 5. Header & Branding
- "USWDS Form Schema Builder & Prototype Generator" → "Form Builder"
- "JSON-Driven Dynamic UX Architecture Sandbox" → "Create and preview government forms"
- Footer: Simplify technical compliance text

### ✅ HIGH PRIORITY IMPROVEMENTS

#### 6. Error Preview Toggle
- Rename button: "Errors: OFF" → "Preview: Normal" / "Preview: With Errors"
- Badge: "VISUAL ERROR ERROR MATRIX ACTIVATED" → "Showing Error Examples"
- Add tooltip/help text explaining purpose

#### 7. Visual Hierarchy
- Improve spacing and breathing room
- Clearer section headings
- Better contrast ratios
- More consistent padding/margins

#### 8. Empty States
- Inspector: "Select any page or form field to edit its properties"
- Make purpose immediately obvious

#### 9. Tree View Improvements
- Use clear icons (consistent system)
- Show required field indicators (*)
- Better hover/selected states

### ✅ MEDIUM PRIORITY POLISH

#### 10. Field Type Indicators
Use icon system instead of text:
- Text input: 📝
- Text area: 📄
- Radio: ⭕
- Checkbox: ☑️
- Dropdown: ▼
- Date: 📅
- File: 📎

#### 11. Accessibility
- Ensure WCAG AA color contrast
- Proper ARIA labels throughout
- Keyboard navigation for tree view
- Focus indicators clearly visible

#### 12. Help Text & Tooltips
Add contextual help where needed:
- Explain intro/review/success page types
- Clarify required vs optional fields
- Explain what "Preview Error States" does

---

## Technical Approach

### File Structure
- **Create:** `sample-form-v2.html` (new file)
- **Preserve:** `sample-form.html` (original unchanged)
- **Format:** Single standalone HTML file (same as original)
- **Dependencies:** CDN USWDS 3.13.0 (same as original)

### Code Changes
- Keep the same JavaScript architecture (proven, functional)
- Maintain three-panel layout (works well)
- Update all user-facing strings
- Improve CSS for better visual hierarchy
- Add ARIA attributes where missing
- Ensure color contrast meets WCAG AA

### Default Schema Changes
Replace the seed data `formSchema` with a realistic example:
- Form title: "Federal Benefits Application"
- Clear, conversational field labels
- Helpful hint text that guides users
- Supportive error messages
- Professional but friendly tone throughout

---

## Copy Guidelines for Implementation

### Tone Principles
✅ **Do:**
- Use "you" and "your" (conversational)
- Be direct and concise
- Explain what to do next
- Be supportive when things go wrong
- Use everyday language

❌ **Don't:**
- Use technical jargon
- Use bureaucratic formality
- Blame the user
- Use meta-language (referencing the system itself)
- Be chatty or use filler words

### Example Transformations

**Labels:**
- "Full Legal Name" → "Your full name"
- "Professional Statement & Justification" → "Why are you applying?"
- "Affiliated Agency Domain" → "Which department?"

**Hints:**
- "Provide full legal naming conventions as registered on official credentials." → "Enter your name as it appears on your ID"
- "Acceptable format parameters restricted to certified PDF variants." → "Upload a PDF file"

**Errors:**
- "Legal name verification entry is required." → "Please enter your name"
- "File integrity parsing failure." → "We couldn't read that file. Please try a different PDF."
- "Status validation verification must be marked." → "Please select an option"

---

## Success Criteria

The rebuilt form builder should:

1. ✅ **Pass the 3-second clarity test:** Any user understands each UI element within 3 seconds
2. ✅ **Pass the jargon test:** Zero unexplained technical terms
3. ✅ **Pass the tone test:** All copy sounds helpful and supportive
4. ✅ **Pass the accessibility test:** WCAG AA compliant, keyboard navigable
5. ✅ **Pass the consistency test:** Patterns align with UX.md principles

---

## Out of Scope (Future Phases)

- List-based options input UI (keep comma-separated for now)
- Advanced keyboard shortcuts
- Multi-file architecture
- Template library
- Inline validation examples (beyond error state preview)
- Drag-and-drop reordering

---

## Implementation Checklist

- [ ] Create sample-form-v2.html
- [ ] Update page title and header
- [ ] Rewrite all interface labels
- [ ] Replace default form schema with realistic content
- [ ] Rewrite all error messages in schema
- [ ] Update error preview toggle UI
- [ ] Improve empty state copy
- [ ] Add field type icons
- [ ] Audit and fix color contrast
- [ ] Add missing ARIA labels
- [ ] Test keyboard navigation
- [ ] Improve visual spacing/hierarchy
- [ ] Add helpful tooltips/hints
- [ ] Update footer copy
- [ ] Test with screen reader (if available)
- [ ] Final UX.md compliance review

---

## Timeline Estimate

**Phase 1 Complete Rebuild:** ~2-3 hours of focused work
- Copy updates: 30 min
- Schema rewrite: 45 min
- UI improvements: 60 min
- Accessibility audit: 30 min
- Testing: 15 min

---

**Brief approved and ready for implementation.**
