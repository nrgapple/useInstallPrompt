# useInstallPrompt ⚛️

> A hook for accessing Google Chrome's [Install](https://developer.mozilla.org/en-US/docs/Web/API/BeforeInstallPromptEvent) button for PWAs.

![](https://user-images.githubusercontent.com/10817537/84545881-17c13580-acce-11ea-900b-61fa192ec566.png)

![](https://user-images.githubusercontent.com/10817537/84545818-f19b9580-accd-11ea-9cfb-a309d72c6350.png)

## [Install](https://www.npmjs.com/package/use-install-prompt)

```bash
npm i use-install-prompt
```

## Usage

```tsx
import React from "react"
import useInstallPrompt from "use-install-prompt"

const App: React.FC = () => {
  const [prompt, promptToInstall] = useInstallPrompt()

  return prompt ? (
    <button onClick={promptToInstall} />
  ) : (
    <h1>Browser not supported.</h1>
  )
}
```

Call `promptToInstall` to show the install prompt in Chrome.

Check if `prompt` is defined to deside whether to show a button or not. (On a supported browser)
