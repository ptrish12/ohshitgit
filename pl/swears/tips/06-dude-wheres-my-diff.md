---
tags: tip
title: O kurwa, próbowałem(am) zrobić diff, ale nic się nie wyświetliło?!
id: dude-wheres-my-diff
order: 6
---

Jeżeli masz pewność, że dokonałeś(aś) zmian w plikach, a mimo to `diff` świeci pustkami, to prawdopodobnie dodałeś(aś) swoje pliki do stagingu i musisz użyć specjalnej flagi.

```git
git diff --staged
```

&macr;\\\_(ツ)\_/&macr; (tak, wiem że to feature, a nie bug, ale to jest kurewsko zaskakujące i nieoczywiste za pierwszym razem, kiedy Ci się to wydarzy!)
