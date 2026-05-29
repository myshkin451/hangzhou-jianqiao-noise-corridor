# Hangzhou Jianqiao Airport Noise Corridor Map

Public site: <https://myshkin451.github.io/hangzhou-jianqiao-noise-corridor/>

一个面向杭州租房、买房人群的双语交互地图，用公开资料和简化模型初筛笕桥机场训练噪声可能影响较大的区域。

A bilingual map for renters and home buyers in Hangzhou, using public sources and a simple screening model to flag areas that may be affected by aircraft training noise around Jianqiao Airport.

## What It Helps With

- Click any location on the map to see a rough risk level.
- Search a neighborhood, compound, road, or metro station.
- Switch between Chinese and English.
- Switch between standard, light, Esri street, satellite, and labeled satellite basemaps.
- Share a selected location with a link.
- Use the on-site checklist before signing a lease or buying a home.

## Important Note

This is **not** an official flight-path map, military source, legal conclusion, engineering report, or decibel contour map.

Military airfields do not publish exact routes, training schedules, or real-time tracks. The map is only a practical first-pass tool: use it to decide where to listen more carefully, then verify on site.

## 中文说明

这个项目适合在看房前做“排雷”：输入或点击一个位置，页面会显示它到推断走廊中心线、到机场中心的大致距离，并给出红色、橙色、黄色或外围的初筛判断。

如果某个小区落在红色或橙色范围内，建议至少在工作日白天、晚间和周末分别去听一次，并询问物业、保安和邻居最近一个月的训练噪声情况。

## English

This project is meant as a first-pass housing check. Search or click a location, and the map estimates its distance to an inferred corridor centerline and to Jianqiao Airport, then labels it red, orange, yellow, or outside the main model.

If a compound falls in the red or orange area, visit at different times before making a housing decision: weekday daytime, evening, and weekend. Ask nearby residents or property staff about recent aircraft noise, not just whether the area is "quiet."

## Sources

- Hangzhou public complaint record: <https://yst.hangzhou.com.cn/question.php?question_id=181113171468>
- Article mentioning Jianqiao runway dimensions: <https://www.cgejournal.com/article/id/9496>
- OpenStreetMap: <https://www.openstreetmap.org/copyright>
- Nominatim usage policy: <https://operations.osmfoundation.org/policies/nominatim/>
- Esri World Imagery attribution guidance: <https://support.esri.com/en-us/knowledge-base/what-is-the-correct-way-to-cite-an-arcgis-online-basema-000012040>

## Privacy

Search requests are sent directly from the browser to Nominatim. Location is used only if you click the location button and grant browser permission. This static site does not collect or store user locations.

## Development

This is a static Leaflet page. To preview locally:

```bash
python3 -m http.server 8765 --bind 127.0.0.1
```

Then open <http://127.0.0.1:8765/>.
