

This theme is built on top of Modus Themes via `modus-themes-theme`,
using modus-themes-generate-palette to derive a full Modus-compatible
palette from the colors used by the light ("Material") variant of
rougier/nano-emacs (https://github.com/rougier/nano-emacs), as defined
in that project's `nano-theme-light.el`.  All the face coverage modus
provides comes for free; the only nano-specific work is the handful of
palette entries and semantic mappings below, which reproduce nano's
restrained set of roles (critical, salient, popout, strong, faded,
subtle, highlight) where color is reserved for links, errors, and
matches, and everything else renders close to the default foreground.

# Installation

```
(use-package nano-like-modus-theme <br>
:vc (:url "https://github.com/benleis1/nano-like-modus") <br>
:config <br>
(load-theme 'nano-like-modus t))
```

To deal with fonts I setup mixed-pitch

```
(defvar my-nano-fixed-pitch-font "Roboto Mono for Powerline"
"Fixed-pitch font family used while the nano-like theme is active.")
(defvar my-nano-variable-pitch-font "Fira Code"
 "Variable-pitch font family used while the nano-like theme is active.")

(use-package mixed-pitch
 :ensure t
 :init
 (set-face-attribute 'variable-pitch nil
                    :font my-nano-variable-pitch-font
                   :height 1.0)
 (set-face-attribute 'fixed-pitch nil
                    :font my-nano-fixede-pitch-font
                   :height 1.0))
```

Sample
![sample](./screenshot.png)

# Code:
