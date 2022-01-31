# Codable 이란?
JSON 데이터를 간편하고 쉽게 Encoding / Decoding 할 수 있게 해주는 프로토콜이다.

보통 JSON 데이터를 직접 다루거나 SwiftyJSON과 같은 라이브러리를 통해 다룰 수 있지만, 
Codable을 이용하면 직접 다루거나 라이브러리를 사용하는 것보다 간편하게 JSON 데이터를 다룰 수 있다.

<b>Codable 은 Decodable 과 Encodable  로 이루어져 있다.</b>

Decodable 과 Encodable 은 프로토콜이다.

### 따라서 Codable 이란?

<b>Encodable & Decodable 프로토콜을 준수하는 프로토콜이다.</b>

Struct, Class, Enum 모두 Codable을 채택할 수 있다.