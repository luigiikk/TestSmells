## Happy Path

```java
@Test
public void shouldProcessPacket() throws IOException, ServletException {
  //given
  given(request.getParameter(PacketApi.PACKET_PARAMETER))
  .willReturn(PACKET);
  given(request.getParameter(PacketApi.TYPE_PARAMETER))
  .willReturn(TYPE);
  //when
  servlet.doGet(request, response);
  //then
  verify(packetDataProcessor).process(PACKET, TYPE);
}