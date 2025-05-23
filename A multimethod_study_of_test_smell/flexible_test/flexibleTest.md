## Flexible Test

```java
public void testDisplayCurrentTime_whenever() {
  // fixture setup
  TimeDisplay sut = new TimeDisplay();

  // exercise SUT
  String result = sut.getCurrentTimeAsHtmlFragment();

  // verify outcome
  Calendar time = new DefaultTimeProvider().getTime();
  StringBuffer expectedTime = new StringBuffer();
  expectedTime.append("<span class=\"tinyBoldText\">");

  if ((time.get(Calendar.HOUR_OF_DAY) == 0)
  && (time.get(Calendar.MINUTE) <= 1)) {
    expectedTime.append( "Midnight");
  } else if ((time.get(Calendar.HOUR_OF_DAY) == 12)
    && (time.get(Calendar.MINUTE) == 0)) { // noon
    expectedTime.append("Noon");
  } else {
    SimpleDateFormat fr = new SimpleDateFormat("h:mm a");
    expectedTime.append(fr.format(time.getTime()));
  }
  expectedTime.append("</span>");
  assertEquals( expectedTime, result);
}