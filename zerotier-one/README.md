# TomCzHen Hass.io Add-ons: ZeroTier One

## 说明

1. 配置 `port` 与 `auth_token`

2. 通过添加 [RESTful Sensor](https://www.home-assistant.io/components/sensor.rest/) 查看 ZeroTier One 状态

- platform: rest
    name: ZeroTier One Status
    json_attributes:
      - address
      - version
    resource: http://127.0.0.1:9993/status
    value_template: '{{ value_json.online }}'
    method: GET
    headers:
      X-ZT1-Auth: yourauthtoken

3. 在 ZeroTier Central 使用 Manually Add Member 添加设备 `address`

## Add-on URL

<https://github.com/TomCzHen/hassio-addon-zerotier-one>