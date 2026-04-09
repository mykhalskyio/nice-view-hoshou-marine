# nice-view-hoshou-marine

![hoshou-marine](./hoshou-marine.gif)

Based on the [nice-view-mod](https://github.com/GPeye/nice-view-mod) template by GPeye.

## Usage

Add this module to your `config/west.yml`:

```yml
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: mykhalskyio                         #new entry
      url-base: https://github.com/mykhalskyio  #new entry
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: nice-view-hoshou-marine        #new entry
      remote: mykhalskyio                  #new entry
      revision: main                       #new entry
  self:
    path: config
```

Then swap the default nice_view shield for the custom one in your `build.yaml`:

```yml
---
include:
  - board: nice_nano_v2
    shield: urchin_left nice_view_adapter nice_view_custom  #custom shield
  - board: nice_nano_v2
    shield: urchin_right nice_view_adapter nice_view_custom #custom shield
```

## Credits

- Pixel art **Hoshou Marine** by [Layke](https://www.pixilart.com/art/hoshou-marine-sr28535439e822e?ft=user&ft_id=f0eff5fb5d001f7) on Pixilart
- Custom nice!view shield template by [GPeye](https://github.com/GPeye/nice-view-mod)

## License

MIT
