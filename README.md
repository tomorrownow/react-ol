# (In Development) react-ol

React component library for OpenLayers.

## Example

```js

<Map center={center} zoom={zoom} projection={projection}>
    <Layers>
        <TileLayer source={nlcdsource} opacity={0.75}/>
        <TileLayer source={osmSource} opacity={0.5}/>
        <VectorTileLayer 
            layerName="counties"
            zIndex={1}
            minZoom={4}
            declutter={true}
            renderMode="vector"
            style={countiesStyleWithLabel}
            source={countySource}
        />
        <VectorTileLayer 
            layerName="seletedCounties" 
            renderMode="vector"
            source={countySource} 
            style={countyStyle}
        />
    </Layers>

    <Controls>
        <FullScreenControl />
        <ZoomSliderControl />
        <ScaleLineControl />
    </Controls>
              
    <Interactions>
        <Draw source={pointSource}></Draw>
    </Interactions>

    <Events>
        <OnMapEvent eventName='click' eventHandler={onClickEvent}></OnMapEvent>
    </Events>
</Map>

```
