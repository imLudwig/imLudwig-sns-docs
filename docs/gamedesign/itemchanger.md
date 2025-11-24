# Itemchanger Item hinzufügen. 

Der Itemchanger ermöglicht es Spielern gewisse Items umzubennen, mit neuen labeln zu versehen oder auch deren Bilder zu beeinflussen. 

Items können Joblocked werden und die Bilder müssen vorgegeben werden. 

<p style="color: #ff7340; border: 1px solid rgba(255, 135, 23, 0.25); border-radius:5px; padding: 1rem;">Bilder funktionieren nur wenn es ein zugehöriges Item gibt, falls du das Item anlegen musst, nutze die bereitgestellt SQL. <br> <br> Auch Kommatas dürfen zwischen den Items nicht fehlen.</p>

## Beispielcode: 

### Joblocked

```lua
    limonade = {
        job = { "winery" }, --Liste von Jobs ODER "caneveryone" als String
        icons = { "limonade", "raspberry_lemonade", "strawberry_lemonade", "applewine", "special_wine", "blackberry_wine" }
    },
```

### ohne Joblock

```lua
    gluecksbringer = {
        job = "caneveryone", --Liste von Jobs ODER "caneveryone" als String
        icons = { "provision_raven_feather", "provision_trinket_asteroid_chunk", "provision_bracelet_gold", "kit_lightning_conductor", "clothing_hl_player_hat_accs", "folder_kit_keepsakes", "provision_trinket_toad_leg", "provision_trinket_wolf_heart", "feathers_plume" }
    },
```

## SQL-Statment um Items für Bilder zu erstellen

```sql
INSERT IGNORE INTO `items` (`item`, `label`, `limit`, `can_remove`, `type`, `usable`, `id`, `groupId`, `metadata`, `desc`, `item_tierlevel`, `item_category`, `craftable`, `weight`, `degradation`) VALUES
('ITEMNAME', 'nicht loeschen', 100, 1, 'item_standard', 1, 0, 1, '{}', 'nur für Bild da', 4, '[{"value":"Sonstiges","name":"something"}]', 1, 1.00, 0)
```
