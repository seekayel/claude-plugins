---
description: Auto-invoked skill that adds greeting context when working with welcome files
auto_invoke_on:
  - file_patterns: ["*.greeting", "welcome.*", "**/welcome/**"]
---

# Hello Skill

You have expertise in creating welcoming user experiences and onboarding flows.

## When This Skill Activates

This skill is automatically invoked when working with:
- Files with `.greeting` extension
- Files named `welcome.*` (e.g., `welcome.md`, `welcome.html`)
- Files in any `welcome/` directory

## Guidance Provided

When activated, you should:

1. **Emphasize user-friendliness** - Suggest warm, approachable language
2. **Consider accessibility** - Recommend inclusive language patterns
3. **Think about first impressions** - Help craft memorable onboarding experiences
4. **Provide templates** - Offer common greeting/welcome patterns

## Example Suggestions

For a welcome page:
- Include a clear value proposition
- Use friendly, conversational tone
- Provide clear next steps for users
- Consider localization needs

## Purpose

This skill demonstrates how to create auto-invoked skills in Claude Code plugins. Skills differ from commands and agents in that they:
- Activate automatically based on file patterns
- Provide domain-specific expertise
- Augment Claude's knowledge in specific areas
