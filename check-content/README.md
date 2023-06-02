	ENTRYPOINT và CMD là hai instruction trong Dockerfile để thiết lập các điểm vào (entry point) và các tham số mặc định cho container khi nó được chạy. Dưới đây là sự khác biệt chính giữa ENTRYPOINT và CMD:

1. ENTRYPOINT:

	ENTRYPOINT xác định một chương trình hoặc một command mà sẽ được chạy khi container được khởi chạy.
	ENTRYPOINT giúp định nghĩa một điểm vào cố định cho container, tức là một command hoặc một ứng dụng chạy liên tục trong container.
	Khi chạy container, các tham số sau ENTRYPOINT sẽ được truyền vào như các đối số cho chương trình được xác định bởi ENTRYPOINT.
	ENTRYPOINT không bị ghi đè bởi command được chỉ định khi chạy container.
2. CMD:

	CMD xác định các tham số mặc định cho command được chỉ định trong ENTRYPOINT hoặc cho command mặc định của container.
	CMD chỉ định các tham số mặc định và không chạy command ngay lập tức khi container được khởi chạy.
	Nếu CMD được chỉ định trong Dockerfile mà không có ENTRYPOINT, CMD sẽ được thực thi như command mặc định của container.
	Nếu CMD được chỉ định trong Dockerfile cùng với ENTRYPOINT, CMD sẽ được sử dụng như các tham số mặc định cho ENTRYPOINT.
