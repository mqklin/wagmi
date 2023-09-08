<script setup>
import { getSidebar } from '../../.vitepress/sidebar'

const actions = getSidebar()['/core']
  .find(x => x.text === 'API').items
  .find(x => x.link === '/core/api/actions').items
  .sort((a, b) => a.text.localeCompare(b.text))
</script>

# Actions

Actions for accounts, wallets, contracts, transactions, signing, ENS, and more.

## Import

```ts
import { getAccount } from '@wagmi/core'
```

## All Actions

<ul>
  <li v-for="action of actions">
    <a :href="action.link">{{ action.text }}</a>
  </li>
</ul>