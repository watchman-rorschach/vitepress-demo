# VitePress 💙 StackBlitz

Hi there :wave: This is a demo running VitePress within your **browser tab**!

## Powered by Vite

VitePress uses Vite under the hood. This means:

asdasdasdasas

## Markdown-Centered

So you can focus more on writing. Powered by MarkdownIt. Comes with many [built-in extensions](https://vitepress.dev/guide/markdown), and you can use Vue features in Markdown too!
商城菜单配置
权限字段太长 可以使用 dbeaver 来查看
运营后台菜单配置

1. 新增菜单，将菜单数据保存到 ms_mc_menu
2. 将菜单权限新增到 平台角色权限 ms_mc_role_auth id=2 的 auth 和 config_auth
3. 由于管理员角色不可修改，需要更新管理员角色喝管理员 auth 将菜单权限新增到 角色权限 ms_mc_member_auth ms_mc_member_role ms_mc_member_user_auth

```
{
"path": "/memberCenter/tranactionAbility/saleOrder/orderStatistics",
"name": "订单收发货统计",
}
父级：销售订单
SELECT id from ms_mc_menu where title='销售订单'



INSERT INTO "public"."ms_mc_menu" ("id", "code", "disabled", "key", "level", "menu_order", "paas_id", "parent_id", "remark", "title", "url", "attrs", "source", "up", "data_auth_config", "admin_status", "buyer_status", "in_vendor_status", "out_vendor_status", "added_status") VALUES (nextval('ms_mc_menu_seq') , '@/memberCenter/tranactionAbility/saleOrder/orderStatistics', 'f', '', 1, 1, NULL, 260, '', '订单收发货统计', '/memberCenter/tranactionAbility/saleOrder/orderStatistics', '{}', 1, NULL, 0, 1, 1, 1, 1, 1);

SELECT id from ms_mc_menu where title='交易'
INSERT INTO "public"."ms_mc_menu" ("id", "code", "disabled", "key", "level", "menu_order", "paas_id", "parent_id", "remark", "title", "url", "attrs", "source", "up", "data_auth_config", "admin_status", "buyer_status", "in_vendor_status", "out_vendor_status", "added_status") VALUES (nextval('ms_mc_menu_seq') , '@/memberCenter/tranactionAbility/orderStatistics', 'f', '', 1, 1, NULL, 82, '', '订单收发货统计', '/memberCenter/tranactionAbility/orderStatistics', '{}', 1, NULL, 0, 1, 1, 1, 1, 1);

SELECT id from ms_mc_menu where title='订单管理';

INSERT INTO "public"."ms_mc_menu" ("id", "code", "disabled", "key", "level", "menu_order", "paas_id", "parent_id", "remark", "title", "url", "attrs", "source", "up", "data_auth_config", "admin_status", "buyer_status", "in_vendor_status", "out_vendor_status", "added_status") VALUES (nextval('ms_mc_menu_seq') , '@/orderSystem/orderStatistics', 'f', '', 1, 1, NULL, 732, '', '订单收发货统计', '/orderSystem/orderStatistics', '{}', 99, NULL, 0, 1, 1, 1, 1, 1);

,{"id": 3066, "url": "/memberCenter/tranactionAbility/saleOrder/orderStatistics", "code": "@/memberCenter/tranactionAbility/saleOrder/orderStatistics", "attrs": {}, "order": 1, "title": "订单收发货统计", "source": 1, "status": 1, "buttons": [], "parentId": 260}

, {"id": 3069, "url": "/memberCenter/tranactionAbility/saleOrder/orderStatistics", "code": "@/memberCenter/tranactionAbility/saleOrder/orderStatistics", "attrs": {}, "order": 1, "title": "订单收发货统计", "source": 1, "status": 1, "buttons": [], "parentId": 82}

,{"id": 3068, "url": "/orderSystem/orderStatistics", "code": "@/orderSystem/orderStatistics", "attrs": {}, "order": 1, "title": "订单收发货统计", "source": 1, "status": 1, "buttons": [], "parentId": 732}
```

urlList.stream().filter(url->url.equals("/authConfig/buyerUserRoleMaintenance")).findFirst()
会员中心菜单配置

1. 新增菜单，将菜单数据保存到 ms_mc_menu
2. 将菜单权限新增到 平台角色权限 ms_mc_role_auth
