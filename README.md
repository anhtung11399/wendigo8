import streamlit as st

# Khởi tạo trạng thái phiên làm việc (session state)
if 'current_page' not in st.session_state:
    st.session_state.current_page = "Trang A"

# Hàm hiển thị trang A
def load_page_a():
    st.header("Trang A")
    # Đặt mã hiển thị trang A ở đây

# Hàm hiển thị trang B
def load_page_b():
    st.header("Trang B")
    # Đặt mã hiển thị trang B ở đây

# Hàm hiển thị trang C
def load_page_c():
    st.header("Trang C")
    # Đặt mã hiển thị trang C ở đây

# Tạo sidebar với 3 nút
if st.button("Trang A"):
    st.session_state.current_page = "Trang A"
if st.button("Trang B"):
    st.session_state.current_page = "Trang B"
if st.button("Trang C"):
    st.session_state.current_page = "Trang C"

# Hiển thị trang tương ứng với trạng thái hiện tại
if st.session_state.current_page == "Trang A":
    load_page_a()
elif st.session_state.current_page == "Trang B":
    load_page_b()
elif st.session_state.current_page == "Trang C":
    load_page_c()
