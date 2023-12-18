## Common Commands

#### Rescale

```shell
ffmpeg -i input.mp4 -vf scale=w:h output.mp4
```

#### Reencode in different `contant rate factor`

```shell
ffmpeg -i input.mp4 -vcodec libx264 -crf 28 output.mp4
```

!!! note
	The range of the quantizer scale is 0-51: **where 0 is lossless, 23 is default, and 51 is worst possible. A _lower_ value is a higher quality** and a subjectively sane range is 18-28. _Consider 18 to be visually lossless_ or nearly so: it should look the same or nearly the same as the input but it isn't technically lossless.