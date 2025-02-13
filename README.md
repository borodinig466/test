var strings = List.of("one", "two", "three", "four", "five");
Gatherer<String, ?, List<String>> slidingWindow =
        Gatherers.windowSliding(2);
var result = strings.stream()
        .gather(slidingWindow)
        .toList();
System.out.println("result = " + result);
