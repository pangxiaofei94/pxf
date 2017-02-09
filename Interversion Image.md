Laravel框架对图片的处理。框架本身没有带对图片的处理，例如 裁剪，缩略...,引入interversion/image就可以了.
1.composer require intervension/image.
2.在config/app.php的providers中加入 "Intervention\Image\ImageServiceProvider::class",在aliases中加入 "'Image' => Intervention\Image\Facades\Image::class"
3.可以直接使用了。
example:

// open an image file
            $img = Image::make('a.jpg');
            // resize image instance
            $img->resize(50, 50);
            // insert a watermark
             $img->insert('public/watermark.png');

            // save image in desired format
            $img->save('new.jpg');
