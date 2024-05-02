---
framework: flutter
platform: Android, iOS, Web, macOS, Linux, Windows
tags: flutter, timeline, flutter timeline v2, timeline tile
title: flutter timeline v2
---

  <meta name="description" content="a fully customizable, ready to use flutter timeline widget">
  <meta name="title" content="flutter timeline widget">

# flutter_timeline [![](https://img.shields.io/badge/pub-latest-brightgreen)](https://pub.dev/packages/flutter_timeline)

![logo](doc/images/logo.png)

Created based on flutter_timeline package from gridaco. I'm just keeping it updated for the flutter community.

> a fully customizable & general timeline widget, based on real-world application references

## Installation

```yaml
dependencies:
  flutter_timeline_v2: latest
```

## usage

_simple_

```dart
  TimelineEventDisplay get plainEventDisplay {
    return TimelineEventDisplay(
        child: TimelineEventCard(
          title: Text("just now"),
          content: Text("someone commented on your timeline ${DateTime.now()}"),
        ),
        indicator: TimelineDots.of(context).circleIcon);
  }

  List<TimelineEventDisplay> events;

  Widget _buildTimeline() {
    return TimelineTheme(
        data: TimelineThemeData(lineColor: Colors.blueAccent),
        child: Timeline(
          indicatorSize: 56,
          events: events,
        ));
  }

  void _addEvent() {
    setState(() {
      events.add(plainEventDisplay);
    });
  }
```

_using offset_

```dart
Widget _buildTimeline() {
  return Timeline(
      indicatorSize: 56,
      events: events,
      altOffset: Offset(0, -24) // set offset
  );
}
```

_using anchor & offset_

```dart
  TimelineEventDisplay get plainEventDisplay {
    return TimelineEventDisplay(
        anchor: IndicatorPosition.top,
        indicatorOffset: Offset(0, 24),
        child: TimelineEventCard(
          title: Text("multi\nline\ntitle\nawesome!"),
          content: Text("someone commented on your timeline ${DateTime.now()}"),
        ),
        indicator: randomIndicator);
  }
```

## complex example

<img src="doc/images/desk-ss-01.png" width="300"/>

## simple example [(run it now!)](https://github.com/naseebnaushad/flutter_timeline_v2/)

<img src="doc/images/mac-ss.png" width="500"/>
<img src="doc/images/mac-ss-2.png" width="500"/>
<img src="doc/images/mac-ss-3.png" width="500"/>

more documentation available at [github](https://github.com/naseebnaushad/flutter_timeline_v2/)


## references

https://www.pinterest.com/official_softmarshmallow/flutter-timeline/
