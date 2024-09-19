# GIS

Một số thuật ngữ:

Level-1:
- Dữ liệu cấp độ 1, thường là dữ liệu đã qua xử lý ban đầu (nhưng không hoàn toàn), bao gồm việc hiệu chỉnh các tín hiệu thô từ vệ tinh thành dữ liệu có thể sử dụng được. Dữ liệu này đã được hiệu chỉnh về quang học hoặc bức xạ nhưng chưa tích hợp với các dữ liệu môi trường khác.

- RA_BD1 đến RA_BD7: Những thuật ngữ này dường như liên quan đến các băng tần (band) hoặc loại dữ liệu được ghi lại từ một cảm biến radar hoặc bức xạ. RA có thể là viết tắt của Radiometric Analysis hoặc Radar Altimeter, BD có thể là Band. Ví dụ:

- RA_BD1 có thể là dữ liệu từ băng tần thứ nhất của cảm biến RA.
- RA_BD2 đến RA_BD7 tương tự như vậy, liên quan đến các băng tần khác nhau của thiết bị.
- IR_SIR: Dữ liệu liên quan đến Infrared Super Spectral Imager (Máy ảnh siêu phổ hồng ngoại), thu nhận dữ liệu hồng ngoại từ nhiều dải phổ.
- IR_UVN: Dữ liệu Infrared Ultraviolet-Near Infrared (Hồng ngoại gần và cực tím), một cảm biến thu thập dữ liệu trong dải sóng từ tia cực tím đến hồng ngoại gần.

Level-2:

   Dữ liệu cấp độ 2 là dữ liệu đã qua xử lý thêm để trích xuất thông tin cụ thể về môi trường hoặc khí hậu. Nó có thể bao gồm các thông số về khí nhà kính, tầng ozone, mây, và các thông tin hóa học khác.

- AER_AI: Aerosol Index - Chỉ số hấp thụ aerosol, đo mức độ ô nhiễm không khí từ các hạt nhỏ trong khí quyển như bụi và khói.
- AER_LH: Aerosol Layer Height - Chiều cao của lớp aerosol trong khí quyển.
- CH4: Methane (CH₄) - Khí metan, một loại khí nhà kính.
- CLOUD: Dữ liệu về mây trong khí quyển, gồm các thông số như độ che phủ, độ dày, và loại mây.
- CO: Carbon Monoxide (CO) - Khí cacbon monoxide, một chất ô nhiễm không khí.
- HCHO: Formaldehyde (HCHO) - Formaldehyde, một chất ô nhiễm hóa học.
- NO2: Nitrogen Dioxide (NO₂) - Khí nitrogen dioxide, một chất ô nhiễm không khí từ nguồn như giao thông và công nghiệp.
- NP_BD3, NP_BD6, NP_BD7: Dữ liệu liên quan đến Near-Polar Band (băng tần gần cực), mỗi băng tần cung cấp thông tin về một dải sóng khác nhau.
- O3: Ozone (O₃) - Dữ liệu về khí ozone trong tầng đối lưu và tầng bình lưu.
- O3_TCL: Ozone Total Column - Tổng lượng ozone trong toàn bộ cột khí quyển.
- O3_PR: Ozone Profile - Hồ sơ ozone, cung cấp thông tin về nồng độ ozone ở các độ cao khác nhau.
- SO2: Sulfur Dioxide (SO₂) - Khí sulfur dioxide, một chất ô nhiễm không khí.

Giải thích các file dữ liệu phụ trợ: 
- AUX_GNSSRD: Auxiliary GNSS Residual Data. Đây là dữ liệu phụ trợ về hệ thống định vị toàn cầu (GNSS - Global Navigation Satellite System). File này chứa thông tin về sai số hoặc dữ liệu hiệu chỉnh tín hiệu GNSS, được sử dụng để cải thiện độ chính xác của phép định vị vệ tinh.
- AUX_PROQUA: Auxiliary Product Quality Data. File này chứa thông tin về chất lượng của sản phẩm dữ liệu chính. Nó có thể bao gồm các thông số đánh giá chất lượng như tỷ lệ tín hiệu/nhiễu, độ chính xác về vị trí, và các thông tin kiểm tra độ chính xác khác.
- AX____POE__AX: Precise Orbit Ephemerides (POE). Đây là dữ liệu về quỹ đạo chính xác của vệ tinh. File này chứa thông tin về vị trí và vận tốc chính xác của vệ tinh trong quá trình hoạt động, giúp hiệu chỉnh các phép đo và dữ liệu thu được.
- AX____ROE__AX: Restituted Orbit Ephemerides (ROE). File này cũng liên quan đến quỹ đạo, nhưng với mức độ chi tiết thấp hơn so với dữ liệu POE. ROE được sử dụng trong quá trình phân tích nhanh và hiệu chỉnh ban đầu dữ liệu vệ tinh.
- AX____MOED_AX: Medium Orbit Ephemerides Data. Đây là dữ liệu quỹ đạo trung bình của vệ tinh. Nó cung cấp các phép đo vị trí và vận tốc vệ tinh với độ chính xác trung bình, có thể được sử dụng trong những trường hợp không yêu cầu độ chính xác cao như POE.
- AUX_COMB: Auxiliary Combined Data. File này chứa các thông tin phụ trợ kết hợp từ nhiều nguồn khác nhau. Nó có thể chứa dữ liệu GNSS, thông tin về quỹ đạo và các thông số môi trường, được tổng hợp lại để cung cấp một bộ dữ liệu hoàn chỉnh cho các nhiệm vụ phân tích và hiệu chỉnh phức tạp.

C-SAR: Hệ thống radar sử dụng băng tần C trên vệ tinh như Sentinel-1.
- Level-0 RAW: Dữ liệu radar thô chưa xử lý.
- Level-1 SLC: Dữ liệu đã qua xử lý ban đầu, có độ phân giải đầy đủ, thường dùng cho phân tích chi tiết.
- Level-1 GRD: Dữ liệu radar đã hiệu chỉnh về tọa độ mặt đất, thích hợp cho các ứng dụng thực địa.
- Level-1 GRD COG: Dữ liệu GRD tối ưu cho lưu trữ và xử lý trên đám mây.
- Level-2 OCN: Dữ liệu liên quan đến các thông số đại dương, như gió và sóng.

Cảm biến trên vệ tinh:
- OLCI: Ocean and Land Colour Instrument

Là một cảm biến đa phổ trên Sentinel-3, được thiết kế để quan sát màu sắc đại dương và đất liền. OLCI có thể thu thập dữ liệu trong nhiều dải quang phổ, giúp giám sát chất lượng nước, sinh khối đại dương, và các đặc điểm liên quan đến thực vật.

- Level-1 EFR: Level-1 Full Resolution Earth Observation
Dữ liệu cấp độ 1, Full Resolution (độ phân giải đầy đủ), là dữ liệu quang phổ từ OLCI đã được xử lý quang học và gắn tọa độ địa lý, nhưng chưa qua xử lý về khí quyển. Dữ liệu này có độ phân giải không gian cao nhất mà cảm biến có thể thu nhận, phù hợp cho các phân tích chi tiết về bề mặt Trái đất và đại dương.
- Level-1 ERR: Level-1 Reduced Resolution Earth Observation
Dữ liệu cấp độ 1, Reduced Resolution (độ phân giải giảm), là dữ liệu quang phổ đã được xử lý tương tự như EFR nhưng ở độ phân giải không gian thấp hơn. Dữ liệu ERR có dung lượng nhỏ hơn và phù hợp cho các ứng dụng cần quan sát quy mô lớn hơn, như theo dõi khí hậu hoặc các khu vực rộng lớn.
- Level-2 LFR: Level-2 Full Resolution Land Product
Dữ liệu cấp độ 2, Full Resolution, dành cho các sản phẩm về đất liền. Đây là dữ liệu đã qua xử lý để loại bỏ các ảnh hưởng của khí quyển và cung cấp thông tin về các chỉ số bề mặt như phản xạ và các chỉ số thực vật (NDVI, EVI). Nó có độ phân giải đầy đủ, dùng cho các phân tích chi tiết về đất liền.
- Level-2 LRR: Level-2 Reduced Resolution Land Product
Dữ liệu cấp độ 2, Reduced Resolution, dành cho các sản phẩm về đất liền với độ phân giải thấp hơn. Dữ liệu này phù hợp cho các ứng dụng yêu cầu quan sát trên phạm vi lớn nhưng không đòi hỏi độ phân giải cao, như theo dõi các biến động môi trường ở quy mô quốc gia hoặc toàn cầu.
- Level-2 WFR: Level-2 Full Resolution Water Product
Dữ liệu cấp độ 2, Full Resolution, dành cho các sản phẩm về đại dương và nước. Dữ liệu này được xử lý để cung cấp các chỉ số như màu sắc nước, độ trong, nhiệt độ bề mặt, và các đặc tính khác của nước với độ phân giải đầy đủ.
- Level-2 WRR: Level-2 Reduced Resolution Water Product
Dữ liệu cấp độ 2, Reduced Resolution, dành cho các sản phẩm về đại dương với độ phân giải thấp hơn. Nó thích hợp cho các ứng dụng cần dữ liệu trên phạm vi rộng, như giám sát đại dương toàn cầu, nhưng không đòi hỏi độ chi tiết cao.

- SRAL: SAR Radar Altimeter

Là một radar đo độ cao sử dụng kỹ thuật Synthetic Aperture Radar (SAR), được sử dụng để đo độ cao mặt nước và đất, thu thập thông tin về mực nước biển, độ cao băng và các thay đổi địa hình.
- SLSTR: Sea and Land Surface Temperature Radiometer

Là cảm biến đo nhiệt độ bề mặt biển và đất liền, được sử dụng để theo dõi biến đổi nhiệt độ trên Trái đất. Nó thu thập dữ liệu trong các dải sóng hồng ngoại và hồng ngoại nhiệt.
- SYNERGY:

Là một tổ hợp dữ liệu từ nhiều cảm biến khác nhau (OLCI, SLSTR), giúp cung cấp thông tin chi tiết hơn về môi trường đất liền và đại dương, kết hợp từ các nguồn dữ liệu khác nhau để tăng độ chính xác.
- Auxiliary Data File (File Dữ liệu Phụ trợ):
Đây là các file hỗ trợ việc xử lý và hiệu chỉnh dữ liệu chính, giúp cải thiện chất lượng và độ chính xác của các sản phẩm dữ liệu vệ tinh.

- AUX_MOEORB: Auxiliary Medium Orbit Ephemeris Data.

Dữ liệu quỹ đạo vệ tinh trung bình, cung cấp thông tin vị trí và tốc độ của vệ tinh với độ chính xác vừa phải.
- AUX_POEORB: Auxiliary Precise Orbit Ephemeris Data.

Dữ liệu quỹ đạo chính xác, được sử dụng cho các phép tính đòi hỏi độ chính xác cao về vị trí và vận tốc vệ tinh.
- AUX_PRCPTF: Auxiliary Precipitation File.

Dữ liệu liên quan đến thông số về lượng mưa, có thể được sử dụng để hiệu chỉnh dữ liệu liên quan đến quan sát bề mặt trong điều kiện có mưa.
- AUX_GNSSRD: Auxiliary GNSS Residual Data.

Dữ liệu phụ trợ từ hệ thống định vị vệ tinh toàn cầu (GNSS), cung cấp thông tin về sai số hoặc hiệu chỉnh từ tín hiệu GNSS, giúp cải thiện độ chính xác của định vị.
- AUX_PROQUA: Auxiliary Product Quality Data 

File chứa dữ liệu đánh giá chất lượng của sản phẩm, bao gồm các chỉ số về độ chính xác, tỷ lệ tín hiệu/nhiễu và các thông số kỹ thuật khác.
- SR___ROE_AX: Restituted Orbit Ephemeris (ROE) 

Dữ liệu quỹ đạo vệ tinh được khôi phục, cung cấp thông tin về quỹ đạo với độ chính xác thấp hơn dữ liệu POE, dùng cho phân tích nhanh.
- SR___MDO_AX: Medium Orbit Ephemeris Data (MDO) 

Dữ liệu quỹ đạo trung bình, cung cấp thông tin vị trí và tốc độ vệ tinh với độ chính xác trung bình.
- SR___POE_AX: Precise Orbit Ephemeris (POE) 

Dữ liệu quỹ đạo chính xác, thường được sử dụng để xử lý dữ liệu có yêu cầu cao về độ chính xác trong xác định vị trí vệ tinh.
- AUX_COMB: Auxiliary Combined Data

Đây là file phụ trợ tổng hợp, chứa thông tin từ nhiều nguồn khác nhau như dữ liệu quỹ đạo, dữ liệu GNSS và các thông số môi trường khác để hỗ trợ việc hiệu chỉnh và phân tích dữ liệu.
