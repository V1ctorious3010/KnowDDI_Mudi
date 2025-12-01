B1: Tạo môi trường
	conda create -n KnowDDI_pytorch python=3.7
	conda install pytorch==1.6.0 torchvision==0.7.0 cudatoolkit=10.2 -c pytorch
	pip install dgl-cu102==0.6.1
	pip install -r requirements.txt
B2: Kích hoạt môi trường: conda activate KnowDDI_pytorch
B3: Chạy code lấy subgraph
Dữ liệu MUDI đã thay thế train/valid/test trong data/Drugbank, nên chạy -e Drugbank thực chất là train trên MUDI.
Trước khi chạy, xóa file digraph_hop_2_BKG_file trong data/Drugbank nếu có
Cách chạy:  cd pytorch → python train.py -e Drugbank