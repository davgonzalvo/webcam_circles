# webcam_circleis
Circle detection from online webcam images

EJERCICIO 1.4

- Hacemos Fork del programa cedido por BetaRobots.
- Hacemos la compilación y creamos el ejecutable
  -Mkdir build
  -.../BUILD/CMAKE ..
  -.../BUILD/MAKE
  
- Una vez ejecutado y ver que funciona correctamente empezamos hacer variaciones en el programa.

- Variamos el color del circulo de detección; tanto el exterior como el interior.

    cv::circle(image, center, 9, cv::Scalar(0,0,0), -1, 8, 0 );// circle center in black
    cv::circle(image, center, radius, cv::Scalar(0,128,128), 3, 8, 0 );// circle perimeter in green
    
- Se puede variar también las constantes: ( tamaño de detección, bordes, distancia,...)

  const int GAUSSIAN_BLUR_SIZE = 7;
  const double GAUSSIAN_BLUR_SIGMA = 2;
  const double CANNY_EDGE_TH = 150;
  const double HOUGH_ACCUM_RESOLUTION = 2;
  const double MIN_CIRCLE_DIST = 80;
  const double HOUGH_ACCUM_TH = 60;
  const int MIN_RADIUS = 20;
  const int MAX_RADIUS = 50;
  
 - Desplazamiento del circulo detección.

     center = cv::Point(cvRound(circles[ii][1]), cvRound(circles[ii][2]));
     radius = cvRound(circles[ii][2]);
     
  

  
