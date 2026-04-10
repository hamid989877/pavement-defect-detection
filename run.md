from ultralytics import YOLO

			
model = YOLO('yolo26x.pt')

			
results = model.train(
    data=f"{dataset.location}/data.yaml",
    epochs=50,
    imgsz=640,
    plots=True,
    device=0,
    batch=32,
    optimizer='MuSGD',
      			
)