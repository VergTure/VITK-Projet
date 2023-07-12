# VITK-Projet

Benjamin CLENE / Yanis FARHAT / Theo BONDI


Ce projet est compose de 3 parties:
- La visualisation d'une image nrrd en 2D
- Le recalage des 2 scans
- La segmentation de la tumeur dans les 2 scans

## 1er partie: La visualisation

Nous avons utilise plt pour afficher les coupes du scan.

Nous l'avons fait en 3D au debut, mais ca nous affichait un block noir en 3D avec la premiere couche du scan.


## 2em partie: Le recalage

Pour le recalage nous avons utiliser la methode de recalage par translation, l'une des fonctions utliser dans le tp.

Pour le groupe, le choix paraissait coherant d'utliser une methode de translation pour recaler les 2 images,
qui sont peu decaler entre elle.

Nous avons rencontrer un probleme pendant l'utilisation de cette fonction.
Plus precisement lorsque l'on voulait utiliser les images repris du nrrd.
Elles n'etaient pas du bon types.
La solution fu de changer le types <class 'itk.itkPyBufferPython.NDArrayITKBase'> en <class 'itk.itkImagePython.itkImageF2'>


## 3em partie: La segmentation

Pour la segmentation nous avons utiliser la methode threshold en mettant nos propres valeurs pour ce derniers
entre 100 et 175, ce qui nous donne des resultats satisfaisant.

## CONCLUSION

Entre les deux scans segmentes, nous pouvons observer une difference de taille entre les 2 tumeurs.
Le scan2 a une tumeurs plus consequentes que le scan1.
Les medecins devraient prendre en considerations ce changements d'etats et intervenir sur ce patient.