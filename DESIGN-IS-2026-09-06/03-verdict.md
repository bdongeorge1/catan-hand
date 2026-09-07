# Verdict: REDESIGN (styling layer)
Total 18/30 is below the 20 threshold, so the rule is REDESIGN; no principle scored 0 and every failure lives in the presentation layer, so the information architecture (3-column card grid, fixed dice bar, bottom reset) is preserved and the visual system is rebuilt from tokens.
## Highest-leverage moves
1. #3 Aesthetic / #7 Long-lasting: replace ad-hoc values with a 4px spacing scale and 5-step type scale; system font; one soft shadow; drop text-shadow and sheen.
2. #8 Thorough / #4: add :focus-visible, aria-disabled minus at 0, prefers-reduced-motion, guard localStorage parse, aria-labels on +/-, aria-live on counts.
3. #2 Useful + a11y: remove maximum-scale=1; darken brick/lumber/ore so labels hit >=4.5:1; flag total >7 (robber discard threshold).
4. #9 Env: remove Google Fonts import (one fewer render-blocking request).
5. #5/#10: landmarks (main/section/footer); calmer press feedback.
