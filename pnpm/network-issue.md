# Network issue with NPM/PNPM

Sometimes npm/pnpm just flat out refuse to work when attempting to install or upgrade packages. This is due to shitty handling of IPv6 either in Node.js or because of npmjs.org. Either way, it can be fixed by using this command

```sh
export NODE_OPTIONS=" --dns-result-order=ipv4first "
```

How is it still a fucking problem in 2024.
