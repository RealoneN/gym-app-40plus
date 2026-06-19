# Gym App — 40+ Men

## Project
Native Android fitness app targeting men over 40. Every exercise screen must display an exercise image. UI theme is dark green throughout.

## Commands
- Build debug APK: `./gradlew assembleDebug`
- Build release APK: `./gradlew assembleRelease`
- Run tests: `./gradlew test`
- Install on device: `./gradlew installDebug`
- Clean: `./gradlew clean`

## Stack
- Language: Kotlin
- Platform: Native Android (Android Studio)
- Min SDK: target devices used by 40+ demographic (API 26+)

## UI Conventions
- Primary color: Dark green (`#1B5E20` or Material `green_900`)
- Theme: Dark green throughout — no light backgrounds
- Every exercise screen MUST include an exercise image (drawable or remote URL)
- Font sizes should be readable for 40+ users — minimum 16sp body text
- High contrast between text and background

## Exercise Screens
- Each exercise must show: name, image, description, sets/reps, safety notes
- Images stored in `res/drawable/` or loaded via Glide/Picasso from URL
- Never show an exercise card without an image placeholder at minimum

## Safe Development Rules
- No force unwrapping (`!!`) without a null check comment explaining why it's safe
- All network calls must handle failure states explicitly
- No hardcoded API keys — use `local.properties` or environment config
- Test on both emulator and physical device before marking a feature done
- Do not modify auto-generated files in `build/` or `.gradle/`

## Project Structure
```
app/
  src/
    main/
      java/         ← Kotlin source
      res/
        drawable/   ← exercise images here
        layout/     ← XML layouts
        values/     ← colors.xml, strings.xml, themes.xml
```
